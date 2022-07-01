#
# project: fips-RenderCore
#
if (NOT FIPS_IMPORT)
    cmake_minimum_required(VERSION 3.0)
	get_filename_component(FIPS_ROOT_DIR "../fips" ABSOLUTE)
	include("${FIPS_ROOT_DIR}/cmake/fips.cmake")
	fips_setup()
    fips_project(fips-RenderCore)
endif()


fips_begin_lib(RenderGraphic)
	fips_vs_disable_warnings(4312)
	#fips_dir(RenderCore)
	fips_files(
		#plugins                            
		RenderCore/AABB.cpp                           
		RenderCore/AABB.hpp                           
		RenderCore/Buffer.hpp                         
		RenderCore/BufferedStream.hpp                 
		RenderCore/CatmullRomInterpolator.hpp         
		RenderCore/checks.hpp                         
		RenderCore/Collection.hpp                     
		RenderCore/Colors.hpp                         
		RenderCore/config.hpp.in    
		RenderCore/config.hpp                  
		RenderCore/CRC32CheckSum.hpp                  
		#DiskDirectory.cpp                  
		#DiskDirectory.hpp                  
		#DiskFile.cpp                       
		#DiskFile.hpp                       
		#FileSystem.cpp                     
		#FileSystem.hpp                     
		RenderCore/Flags.hpp                          
		RenderCore/GlobalSettings.cpp                 
		RenderCore/GlobalSettings.hpp                 
		RenderCore/glsl_math.hpp                      
		#GZipCodec.cpp                      
		#GZipCodec.hpp                      
		RenderCore/half.hpp                           
		#Image.cpp                          
		#Image.hpp                          
		#ImageTools.hpp                     
		RenderCore/IMutex.hpp                         
		RenderCore/Interpolator.hpp                   
		RenderCore/KeyValues.cpp                      
		RenderCore/KeyValues.hpp                      
		RenderCore/LinearInterpolator.hpp             
		RenderCore/link_config.hpp                    
		#LoadWriterManager.cpp              
		#LoadWriterManager.hpp              
		#Log.cpp                            
		#Log.hpp                            
		RenderCore/math_utils.cpp                     
		RenderCore/math_utils.hpp                     
		RenderCore/Matrix2.hpp                        
		RenderCore/Matrix3.hpp                        
		RenderCore/Matrix4.hpp                        
		RenderCore/MD5CheckSum.cpp                    
		RenderCore/MD5CheckSum.hpp              
		RenderCore/MersenneTwister.hpp                
		RenderCore/MurmurHash3.cpp                    
		RenderCore/MurmurHash3.hpp                    
		RenderCore/Object.cpp                         
		RenderCore/Object.hpp                         
		RenderCore/OpenGLDefs.hpp                     
		#RenderCore/pimpl.cpp                          
		RenderCore/Plane.cpp                          
		RenderCore/Plane.hpp                          
		RenderCore/Quaternion.hpp                     
		RenderCore/Random.cpp                         
		RenderCore/Random.hpp                         
		RenderCore/Ray.hpp                            
		RenderCore/Rect.hpp                           
		RenderCore/ResourceDatabase.cpp               
		RenderCore/ResourceDatabase.hpp               
		RenderCore/ResourceLoadWriter.hpp                        
		RenderCore/ScopedMutex.hpp                    
		RenderCore/SignalSlot.hpp                     
		RenderCore/SignalSlotX.hpp                    
		RenderCore/Sphere.hpp                         
		RenderCore/std_types.hpp                          
		RenderCore/Time.cpp                           
		RenderCore/Time.hpp                           
		RenderCore/Transform.cpp                      
		RenderCore/Transform.hpp                      
		RenderCore/TypeInfo.hpp                       
		RenderCore/UUID.cpp                           
		RenderCore/UUID.hpp                           
		RenderCore/Vector2.hpp                        
		RenderCore/Vector3.hpp                        
		RenderCore/Vector4.hpp                               
		RenderCore/vlnamespace.hpp                    
		RenderCore/md5.c
		RenderCore/md5.h
    	)

	fips_deps(Gfx Assets)
fips_end_lib() 


if (NOT FIPS_IMPORT)
    fips_finish()
endif()

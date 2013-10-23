from distutils.core import setup  
import py2exe  
import sys  
includes = ["encodings", "encodings.*"]    
sys.argv.append("py2exe")  
options = {"py2exe":   { "bundle_files": 1 }    
                }   
setup(version = "1.0",
      description = "Struct Extractor with Macros.",
      name = r"StructExtractor",
      options = {"py2exe": {"compressed": 1,  
                            "optimize": 2,  
                            "ascii": 0,  
                            "bundle_files": 1}},
      zipfile=None,
      console = [{"script":'StructExtractormt.py', "icon_resources": [(1, r"extractor.ico")]}] 
      )

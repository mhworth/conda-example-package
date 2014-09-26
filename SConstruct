
env = Environment(CPPPATH='include', LIBPATH='lib')
fancylib1 = env.SharedLibrary('lib/fancylib1', ['src/fancylib/fancylib1.cpp'])
fancylib2 = env.SharedLibrary('lib/fancylib2', ['src/fancylib/fancylib2.cpp'])
main = env.Program('bin/test', ['src/main.cpp'] + [fancylib1, fancylib2])

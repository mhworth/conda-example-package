
AddOption('--prefix',
          dest='prefix',
          type='string',
          nargs=1,
          action='store',
          metavar='DIR',
          help='installation prefix')

env = Environment(CPPPATH='include', LIBPATH='lib', PREFIX=GetOption('prefix'))
fancylib1 = env.SharedLibrary('lib/fancylib1', ['src/fancylib/fancylib1.cpp'])
fancylib2 = env.SharedLibrary('lib/fancylib2', ['src/fancylib/fancylib2.cpp'])
main = env.Program('bin/test', ['src/main.cpp'] + [fancylib1, fancylib2])

install_libs = env.Install('$PREFIX/lib', [fancylib1, fancylib2])
install_bin = env.Install('$PREFIX/bin', [main])
Alias('install-lib', install_libs)
Alias('install-bin', install_bin)
Alias('install', ['install-bin', 'install-lib'])

Default(main)

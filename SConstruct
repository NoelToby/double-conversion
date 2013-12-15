double_conversion_sources = ['src/' + x for x in SConscript('src/SConscript')]
double_conversion_test_sources = ['test/cctest/' + x for x in SConscript('test/cctest/SConscript')]
env = Environment(CPPPATH='#/src', LIBS=['m', 'stdc++'])
debug = ARGUMENTS.get('debug', 0)
optimize = ARGUMENTS.get('optimize', 0)
if int(debug):
  env.Append(CCFLAGS = '-g -Wall -Werror')
if int(optimize):
  env.Append(CCFLAGS = '-O3 -Wall -Werror')
env.Program('run_tests', double_conversion_sources + double_conversion_test_sources)

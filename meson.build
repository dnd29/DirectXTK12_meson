project('directxtk12', 'c', version: '2025.3.21.3')

# 옵션 가져오기
target_platform = get_option('platform')
message('Target platform: ' + target_platform)
target_arch = get_option('arch')
if target_arch == 'any'
	target_arch = 'x64'
endif
buildtype = get_option('buildtype')

build_type_directory_string = 'Release'
if buildtype == 'debug'
    build_type_directory_string = 'Debug'
endif

lib_path = join_paths(meson.current_source_dir(), './native/lib/@0@/@1@/'.format(target_arch, build_type_directory_string))

directxtk12_dep = declare_dependency(
    include_directories: include_directories('./include'),
    link_args: [ lib_path + 'DirectXTK12.lib']
)
.. SPDX-License-Identifier: CC-BY-SA-2.0-UK

******************
Variables Glossary
******************

This chapter lists common variables used in the OpenEmbedded build
system and gives an overview of their function and contents.

..
   check_glossary_begin

:term:`A <ABIEXTENSION>` :term:`B` :term:`C <CACHE>`
:term:`D` :term:`E <EFI_ARCH>` :term:`F <FAKEROOT>`
:term:`G <GCCPIE>` :term:`H <HGDIR>` :term:`I <IMAGE_BASENAME>`
:term:`K <KARCH>` :term:`L <LABELS>` :term:`M <MACHINE>`
:term:`N <NATIVELSBSTRING>` :term:`O <OBJCOPY>` :term:`P`
:term:`Q <QA_EMPTY_DIRS>` :term:`R <RANLIB>` :term:`S` :term:`T`
:term:`U <UBOOT_BINARY>` :term:`V <VIRTUAL-RUNTIME>`
:term:`W <WARN_QA>` :term:`X <XSERVER>` :term:`Z <ZSTD_COMPRESSION_LEVEL>`

..
   check_glossary_end

.. glossary::
   :sorted:

   :term:`ABIEXTENSION`
      .. include:: variables/ABIEXTENSION.rst

   :term:`ALLOW_EMPTY`
      .. include:: variables/ALLOW_EMPTY.rst

   :term:`ALTERNATIVE`
      .. include:: variables/ALTERNATIVE.rst

   :term:`ALTERNATIVE_LINK_NAME`
      .. include:: variables/ALTERNATIVE_LINK_NAME.rst

   :term:`ALTERNATIVE_PRIORITY`
      .. include:: variables/ALTERNATIVE_PRIORITY.rst

   :term:`ALTERNATIVE_TARGET`
      .. include:: variables/ALTERNATIVE_TARGET.rst

   :term:`ANY_OF_DISTRO_FEATURES`
      .. include:: variables/ANY_OF_DISTRO_FEATURES.rst

   :term:`APPEND`
      .. include:: variables/APPEND.rst

   :term:`AR`
      .. include:: variables/AR.rst

   :term:`ARCHIVER_MODE`
      .. include:: variables/ARCHIVER_MODE.rst

   :term:`AS`
      .. include:: variables/AS.rst

   :term:`ASSUME_PROVIDED`
      .. include:: variables/ASSUME_PROVIDED.rst

   :term:`ASSUME_SHLIBS`
      .. include:: variables/ASSUME_SHLIBS.rst

   :term:`AUTO_LIBNAME_PKGS`
      .. include:: variables/AUTO_LIBNAME_PKGS.rst

   :term:`AUTO_SYSLINUXMENU`
      .. include:: variables/AUTO_SYSLINUXMENU.rst

   :term:`AUTOREV`
      .. include:: variables/AUTOREV.rst

   :term:`AUTOTOOLS_SCRIPT_PATH`
      .. include:: variables/AUTOTOOLS_SCRIPT_PATH.rst

   :term:`AVAILTUNES`
      .. include:: variables/AVAILTUNES.rst

   :term:`AZ_SAS`
      .. include:: variables/AZ_SAS.rst

   :term:`B`
      .. include:: variables/B.rst

   :term:`BAD_RECOMMENDATIONS`
      .. include:: variables/BAD_RECOMMENDATIONS.rst

   :term:`BAREBOX_BINARY`
      .. include:: variables/BAREBOX_BINARY.rst

   :term:`BAREBOX_CONFIG`
      .. include:: variables/BAREBOX_CONFIG.rst

   :term:`BASE_LIB`
      .. include:: variables/BASE_LIB.rst

   :term:`BASE_WORKDIR`
      .. include:: variables/BASE_WORKDIR.rst

   :term:`BB_ALLOWED_NETWORKS`
      .. include:: variables/BB_ALLOWED_NETWORKS.rst

   :term:`BB_BASEHASH_IGNORE_VARS`
      .. include:: variables/BB_BASEHASH_IGNORE_VARS.rst

   :term:`BB_CACHEDIR`
      .. include:: variables/BB_CACHEDIR.rst

   :term:`BB_CHECK_SSL_CERTS`
      .. include:: variables/BB_CHECK_SSL_CERTS.rst

   :term:`BB_CONF_FRAGMENT_DESCRIPTION`
      .. include:: variables/BB_CONF_FRAGMENT_DESCRIPTION.rst

   :term:`BB_CONF_FRAGMENT_SUMMARY`
      .. include:: variables/BB_CONF_FRAGMENT_SUMMARY.rst

   :term:`BB_CONSOLELOG`
      .. include:: variables/BB_CONSOLELOG.rst

   :term:`BB_CURRENT_MC`
      .. include:: variables/BB_CURRENT_MC.rst

   :term:`BB_CURRENTTASK`
      .. include:: variables/BB_CURRENTTASK.rst

   :term:`BB_DEFAULT_TASK`
      .. include:: variables/BB_DEFAULT_TASK.rst

   :term:`BB_DEFAULT_UMASK`
      .. include:: variables/BB_DEFAULT_UMASK.rst

   :term:`BB_DEFER_BBCLASSES`
      .. include:: variables/BB_DEFER_BBCLASSES.rst

   :term:`BB_DISKMON_DIRS`
      .. include:: variables/BB_DISKMON_DIRS.rst

   :term:`BB_DISKMON_WARNINTERVAL`
      .. include:: variables/BB_DISKMON_WARNINTERVAL.rst

   :term:`BB_ENV_PASSTHROUGH`
      .. include:: variables/BB_ENV_PASSTHROUGH.rst

   :term:`BB_ENV_PASSTHROUGH_ADDITIONS`
      .. include:: variables/BB_ENV_PASSTHROUGH_ADDITIONS.rst

   :term:`BB_FETCH_PREMIRRORONLY`
      .. include:: variables/BB_FETCH_PREMIRRORONLY.rst

   :term:`BB_FILENAME`
      .. include:: variables/BB_FILENAME.rst

   :term:`BB_GENERATE_MIRROR_TARBALLS`
      .. include:: variables/BB_GENERATE_MIRROR_TARBALLS.rst

   :term:`BB_GENERATE_SHALLOW_TARBALLS`
      .. include:: variables/BB_GENERATE_SHALLOW_TARBALLS.rst

   :term:`BB_GIT_DEFAULT_DESTSUFFIX`
      .. include:: variables/BB_GIT_DEFAULT_DESTSUFFIX.rst

   :term:`BB_GIT_SHALLOW`
      .. include:: variables/BB_GIT_SHALLOW.rst

   :term:`BB_GIT_SHALLOW_DEPTH`
      .. include:: variables/BB_GIT_SHALLOW_DEPTH.rst

   :term:`BB_HASHCHECK_FUNCTION`
      .. include:: variables/BB_HASHCHECK_FUNCTION.rst

   :term:`BB_HASHCONFIG_IGNORE_VARS`
      .. include:: variables/BB_HASHCONFIG_IGNORE_VARS.rst

   :term:`BB_HASHSERVE`
      .. include:: variables/BB_HASHSERVE.rst

   :term:`BB_HASHSERVE_UPSTREAM`
      .. include:: variables/BB_HASHSERVE_UPSTREAM.rst

   :term:`BB_INVALIDCONF`
      .. include:: variables/BB_INVALIDCONF.rst

   :term:`BB_LOADFACTOR_MAX`
      .. include:: variables/BB_LOADFACTOR_MAX.rst

   :term:`BB_LOGCONFIG`
      .. include:: variables/BB_LOGCONFIG.rst

   :term:`BB_LOGFMT`
      .. include:: variables/BB_LOGFMT.rst

   :term:`BB_MULTI_PROVIDER_ALLOWED`
      .. include:: variables/BB_MULTI_PROVIDER_ALLOWED.rst

   :term:`BB_NICE_LEVEL`
      .. include:: variables/BB_NICE_LEVEL.rst

   :term:`BB_NO_NETWORK`
      .. include:: variables/BB_NO_NETWORK.rst

   :term:`BB_NUMBER_PARSE_THREADS`
      .. include:: variables/BB_NUMBER_PARSE_THREADS.rst

   :term:`BB_NUMBER_THREADS`
      .. include:: variables/BB_NUMBER_THREADS.rst

   :term:`BB_ORIGENV`
      .. include:: variables/BB_ORIGENV.rst

   :term:`BB_PRESERVE_ENV`
      .. include:: variables/BB_PRESERVE_ENV.rst

   :term:`BB_PRESSURE_MAX_CPU`
      .. include:: variables/BB_PRESSURE_MAX_CPU.rst

   :term:`BB_PRESSURE_MAX_IO`
      .. include:: variables/BB_PRESSURE_MAX_IO.rst

   :term:`BB_PRESSURE_MAX_MEMORY`
      .. include:: variables/BB_PRESSURE_MAX_MEMORY.rst

   :term:`BB_RUNFMT`
      .. include:: variables/BB_RUNFMT.rst

   :term:`BB_RUNTASK`
      .. include:: variables/BB_RUNTASK.rst

   :term:`BB_SCHEDULER`
      .. include:: variables/BB_SCHEDULER.rst

   :term:`BB_SCHEDULERS`
      .. include:: variables/BB_SCHEDULERS.rst

   :term:`BB_SERVER_TIMEOUT`
      .. include:: variables/BB_SERVER_TIMEOUT.rst

   :term:`BB_SETSCENE_DEPVALID`
      .. include:: variables/BB_SETSCENE_DEPVALID.rst

   :term:`BB_SIGNATURE_EXCLUDE_FLAGS`
      .. include:: variables/BB_SIGNATURE_EXCLUDE_FLAGS.rst

   :term:`BB_SIGNATURE_HANDLER`
      .. include:: variables/BB_SIGNATURE_HANDLER.rst

   :term:`BB_SRCREV_POLICY`
      .. include:: variables/BB_SRCREV_POLICY.rst

   :term:`BB_STRICT_CHECKSUM`
      .. include:: variables/BB_STRICT_CHECKSUM.rst

   :term:`BB_TASK_IONICE_LEVEL`
      .. include:: variables/BB_TASK_IONICE_LEVEL.rst

   :term:`BB_TASK_NICE_LEVEL`
      .. include:: variables/BB_TASK_NICE_LEVEL.rst

   :term:`BB_TASKHASH`
      .. include:: variables/BB_TASKHASH.rst

   :term:`BB_USE_HOME_NPMRC`
      .. include:: variables/BB_USE_HOME_NPMRC.rst

   :term:`BB_VERBOSE_LOGS`
      .. include:: variables/BB_VERBOSE_LOGS.rst

   :term:`BB_WORKERCONTEXT`
      .. include:: variables/BB_WORKERCONTEXT.rst

   :term:`BBCLASSEXTEND`
      .. include:: variables/BBCLASSEXTEND.rst

   :term:`BBDEBUG`
      .. include:: variables/BBDEBUG.rst

   :term:`BBFILE_COLLECTIONS`
      .. include:: variables/BBFILE_COLLECTIONS.rst

   :term:`BBFILE_PATTERN`
      .. include:: variables/BBFILE_PATTERN.rst

   :term:`BBFILE_PRIORITY`
      .. include:: variables/BBFILE_PRIORITY.rst

   :term:`BBFILES`
      .. include:: variables/BBFILES.rst

   :term:`BBFILES_DYNAMIC`
      .. include:: variables/BBFILES_DYNAMIC.rst

   :term:`BBINCLUDED`
      .. include:: variables/BBINCLUDED.rst

   :term:`BBINCLUDELOGS`
      .. include:: variables/BBINCLUDELOGS.rst

   :term:`BBINCLUDELOGS_LINES`
      .. include:: variables/BBINCLUDELOGS_LINES.rst

   :term:`BBLAYERS`
      .. include:: variables/BBLAYERS.rst

   :term:`BBLAYERS_FETCH_DIR`
      .. include:: variables/BBLAYERS_FETCH_DIR.rst

   :term:`BBMASK`
      .. include:: variables/BBMASK.rst

   :term:`BBMULTICONFIG`
      .. include:: variables/BBMULTICONFIG.rst

   :term:`BBPATH`
      .. include:: variables/BBPATH.rst

   :term:`BBSERVER`
      .. include:: variables/BBSERVER.rst

   :term:`BBTARGETS`
      .. include:: variables/BBTARGETS.rst

   :term:`BINCONFIG`
      .. include:: variables/BINCONFIG.rst

   :term:`BINCONFIG_GLOB`
      .. include:: variables/BINCONFIG_GLOB.rst

   :term:`BITBAKE_UI`
      .. include:: variables/BITBAKE_UI.rst

   :term:`BP`
      .. include:: variables/BP.rst

   :term:`BPN`
      .. include:: variables/BPN.rst

   :term:`BUGTRACKER`
      .. include:: variables/BUGTRACKER.rst

   :term:`BUILD_AR`
      .. include:: variables/BUILD_AR.rst

   :term:`BUILD_ARCH`
      .. include:: variables/BUILD_ARCH.rst

   :term:`BUILD_AS`
      .. include:: variables/BUILD_AS.rst

   :term:`BUILD_AS_ARCH`
      .. include:: variables/BUILD_AS_ARCH.rst

   :term:`BUILD_CC`
      .. include:: variables/BUILD_CC.rst

   :term:`BUILD_CC_ARCH`
      .. include:: variables/BUILD_CC_ARCH.rst

   :term:`BUILD_CCLD`
      .. include:: variables/BUILD_CCLD.rst

   :term:`BUILD_CFLAGS`
      .. include:: variables/BUILD_CFLAGS.rst

   :term:`BUILD_CPP`
      .. include:: variables/BUILD_CPP.rst

   :term:`BUILD_CPPFLAGS`
      .. include:: variables/BUILD_CPPFLAGS.rst

   :term:`BUILD_CXX`
      .. include:: variables/BUILD_CXX.rst

   :term:`BUILD_CXXFLAGS`
      .. include:: variables/BUILD_CXXFLAGS.rst

   :term:`BUILD_FC`
      .. include:: variables/BUILD_FC.rst

   :term:`BUILD_LD`
      .. include:: variables/BUILD_LD.rst

   :term:`BUILD_LD_ARCH`
      .. include:: variables/BUILD_LD_ARCH.rst

   :term:`BUILD_LDFLAGS`
      .. include:: variables/BUILD_LDFLAGS.rst

   :term:`BUILD_NM`
      .. include:: variables/BUILD_NM.rst

   :term:`BUILD_OBJCOPY`
      .. include:: variables/BUILD_OBJCOPY.rst

   :term:`BUILD_OBJDUMP`
      .. include:: variables/BUILD_OBJDUMP.rst

   :term:`BUILD_OPTIMIZATION`
      .. include:: variables/BUILD_OPTIMIZATION.rst

   :term:`BUILD_OS`
      .. include:: variables/BUILD_OS.rst

   :term:`BUILD_PREFIX`
      .. include:: variables/BUILD_PREFIX.rst

   :term:`BUILD_RANLIB`
      .. include:: variables/BUILD_RANLIB.rst

   :term:`BUILD_READELF`
      .. include:: variables/BUILD_READELF.rst

   :term:`BUILD_STRIP`
      .. include:: variables/BUILD_STRIP.rst

   :term:`BUILD_SYS`
      .. include:: variables/BUILD_SYS.rst

   :term:`BUILD_VENDOR`
      .. include:: variables/BUILD_VENDOR.rst

   :term:`BUILDDIR`
      .. include:: variables/BUILDDIR.rst

   :term:`BUILDHISTORY_COMMIT`
      .. include:: variables/BUILDHISTORY_COMMIT.rst

   :term:`BUILDHISTORY_COMMIT_AUTHOR`
      .. include:: variables/BUILDHISTORY_COMMIT_AUTHOR.rst

   :term:`BUILDHISTORY_DIR`
      .. include:: variables/BUILDHISTORY_DIR.rst

   :term:`BUILDHISTORY_FEATURES`
      .. include:: variables/BUILDHISTORY_FEATURES.rst

   :term:`BUILDHISTORY_IMAGE_FILES`
      .. include:: variables/BUILDHISTORY_IMAGE_FILES.rst

   :term:`BUILDHISTORY_PATH_PREFIX_STRIP`
      .. include:: variables/BUILDHISTORY_PATH_PREFIX_STRIP.rst

   :term:`BUILDHISTORY_PUSH_REPO`
      .. include:: variables/BUILDHISTORY_PUSH_REPO.rst

   :term:`BUILDNAME`
      .. include:: variables/BUILDNAME.rst

   :term:`BUILDSDK_CFLAGS`
      .. include:: variables/BUILDSDK_CFLAGS.rst

   :term:`BUILDSDK_CPPFLAGS`
      .. include:: variables/BUILDSDK_CPPFLAGS.rst

   :term:`BUILDSDK_CXXFLAGS`
      .. include:: variables/BUILDSDK_CXXFLAGS.rst

   :term:`BUILDSDK_LDFLAGS`
      .. include:: variables/BUILDSDK_LDFLAGS.rst

   :term:`BUILDSTATS_BASE`
      .. include:: variables/BUILDSTATS_BASE.rst

   :term:`BUSYBOX_SPLIT_SUID`
      .. include:: variables/BUSYBOX_SPLIT_SUID.rst

   :term:`CACHE`
      .. include:: variables/CACHE.rst

   :term:`CARGO_INSTALL_LIBRARIES`
      .. include:: variables/CARGO_INSTALL_LIBRARIES.rst

   :term:`CC`
      .. include:: variables/CC.rst

   :term:`CCACHE_DISABLE`
      .. include:: variables/CCACHE_DISABLE.rst

   :term:`CCACHE_NATIVE_RECIPES_ALLOWED`
      .. include:: variables/CCACHE_NATIVE_RECIPES_ALLOWED.rst

   :term:`CCACHE_TOP_DIR`
      .. include:: variables/CCACHE_TOP_DIR.rst

   :term:`CCLD`
      .. include:: variables/CCLD.rst

   :term:`CFLAGS`
      .. include:: variables/CFLAGS.rst

   :term:`CHECKLAYER_REQUIRED_TESTS`
      .. include:: variables/CHECKLAYER_REQUIRED_TESTS.rst

   :term:`CLASSOVERRIDE`
      .. include:: variables/CLASSOVERRIDE.rst

   :term:`CLEANBROKEN`
      .. include:: variables/CLEANBROKEN.rst

   :term:`COMBINED_FEATURES`
      .. include:: variables/COMBINED_FEATURES.rst

   :term:`COMMERCIAL_AUDIO_PLUGINS`
      .. include:: variables/COMMERCIAL_AUDIO_PLUGINS.rst

   :term:`COMMERCIAL_VIDEO_PLUGINS`
      .. include:: variables/COMMERCIAL_VIDEO_PLUGINS.rst

   :term:`COMMON_LICENSE_DIR`
      .. include:: variables/COMMON_LICENSE_DIR.rst

   :term:`COMPATIBLE_HOST`
      .. include:: variables/COMPATIBLE_HOST.rst

   :term:`COMPATIBLE_MACHINE`
      .. include:: variables/COMPATIBLE_MACHINE.rst

   :term:`COMPLEMENTARY_GLOB`
      .. include:: variables/COMPLEMENTARY_GLOB.rst

   :term:`COMPONENTS_DIR`
      .. include:: variables/COMPONENTS_DIR.rst

   :term:`CONF_VERSION`
      .. include:: variables/CONF_VERSION.rst

   :term:`CONFFILES`
      .. include:: variables/CONFFILES.rst

   :term:`CONFIG_INITRAMFS_SOURCE`
      .. include:: variables/CONFIG_INITRAMFS_SOURCE.rst

   :term:`CONFIG_SITE`
      .. include:: variables/CONFIG_SITE.rst

   :term:`CONFIGURE_FLAGS`
      .. include:: variables/CONFIGURE_FLAGS.rst

   :term:`CONFIGURE_SCRIPT`
      .. include:: variables/CONFIGURE_SCRIPT.rst

   :term:`CONFLICT_COMBINED_FEATURES`
      .. include:: variables/CONFLICT_COMBINED_FEATURES.rst

   :term:`CONFLICT_DISTRO_FEATURES`
      .. include:: variables/CONFLICT_DISTRO_FEATURES.rst

   :term:`CONFLICT_IMAGE_FEATURES`
      .. include:: variables/CONFLICT_IMAGE_FEATURES.rst

   :term:`CONFLICT_MACHINE_FEATURES`
      .. include:: variables/CONFLICT_MACHINE_FEATURES.rst

   :term:`CONFLICT_TUNE_FEATURES`
      .. include:: variables/CONFLICT_TUNE_FEATURES.rst

   :term:`CONVERSION_CMD`
      .. include:: variables/CONVERSION_CMD.rst

   :term:`COPY_LIC_DIRS`
      .. include:: variables/COPY_LIC_DIRS.rst

   :term:`COPY_LIC_MANIFEST`
      .. include:: variables/COPY_LIC_MANIFEST.rst

   :term:`COPYLEFT_LICENSE_EXCLUDE`
      .. include:: variables/COPYLEFT_LICENSE_EXCLUDE.rst

   :term:`COPYLEFT_LICENSE_INCLUDE`
      .. include:: variables/COPYLEFT_LICENSE_INCLUDE.rst

   :term:`COPYLEFT_PN_EXCLUDE`
      .. include:: variables/COPYLEFT_PN_EXCLUDE.rst

   :term:`COPYLEFT_PN_INCLUDE`
      .. include:: variables/COPYLEFT_PN_INCLUDE.rst

   :term:`COPYLEFT_RECIPE_TYPES`
      .. include:: variables/COPYLEFT_RECIPE_TYPES.rst

   :term:`CORE_IMAGE_EXTRA_INSTALL`
      .. include:: variables/CORE_IMAGE_EXTRA_INSTALL.rst

   :term:`COREBASE`
      .. include:: variables/COREBASE.rst

   :term:`COREBASE_FILES`
      .. include:: variables/COREBASE_FILES.rst

   :term:`CPP`
      .. include:: variables/CPP.rst

   :term:`CPPFLAGS`
      .. include:: variables/CPPFLAGS.rst

   :term:`CROSS_COMPILE`
      .. include:: variables/CROSS_COMPILE.rst

   :term:`CVE_CHECK_IGNORE`
      .. include:: variables/CVE_CHECK_IGNORE.rst

   :term:`CVE_CHECK_MANIFEST_JSON`
      .. include:: variables/CVE_CHECK_MANIFEST_JSON.rst

   :term:`CVE_CHECK_SKIP_RECIPE`
      .. include:: variables/CVE_CHECK_SKIP_RECIPE.rst

   :term:`CVE_CHECK_STATUSMAP`
      .. include:: variables/CVE_CHECK_STATUSMAP.rst

   :term:`CVE_CHECK_VEX_JUSTIFICATION`
      .. include:: variables/CVE_CHECK_VEX_JUSTIFICATION.rst

   :term:`CVE_PRODUCT`
      .. include:: variables/CVE_PRODUCT.rst

   :term:`CVE_STATUS`
      .. include:: variables/CVE_STATUS.rst

   :term:`CVE_STATUS_GROUPS`
      .. include:: variables/CVE_STATUS_GROUPS.rst

   :term:`CVE_VERSION`
      .. include:: variables/CVE_VERSION.rst

   :term:`CVSDIR`
      .. include:: variables/CVSDIR.rst

   :term:`CXX`
      .. include:: variables/CXX.rst

   :term:`CXXFLAGS`
      .. include:: variables/CXXFLAGS.rst

   :term:`D`
      .. include:: variables/D.rst

   :term:`DATE`
      .. include:: variables/DATE.rst

   :term:`DATETIME`
      .. include:: variables/DATETIME.rst

   :term:`DEBIAN_NOAUTONAME`
      .. include:: variables/DEBIAN_NOAUTONAME.rst

   :term:`DEBIANNAME`
      .. include:: variables/DEBIANNAME.rst

   :term:`DEBUG_BUILD`
      .. include:: variables/DEBUG_BUILD.rst

   :term:`DEBUG_OPTIMIZATION`
      .. include:: variables/DEBUG_OPTIMIZATION.rst

   :term:`DEBUG_PREFIX_MAP`
      .. include:: variables/DEBUG_PREFIX_MAP.rst

   :term:`DEFAULT_PREFERENCE`
      .. include:: variables/DEFAULT_PREFERENCE.rst

   :term:`DEFAULT_TIMEZONE`
      .. include:: variables/DEFAULT_TIMEZONE.rst

   :term:`DEFAULTTUNE`
      .. include:: variables/DEFAULTTUNE.rst

   :term:`DEPENDS`
      .. include:: variables/DEPENDS.rst

   :term:`DEPLOY_DIR`
      .. include:: variables/DEPLOY_DIR.rst

   :term:`DEPLOY_DIR_DEB`
      .. include:: variables/DEPLOY_DIR_DEB.rst

   :term:`DEPLOY_DIR_IMAGE`
      .. include:: variables/DEPLOY_DIR_IMAGE.rst

   :term:`DEPLOY_DIR_IPK`
      .. include:: variables/DEPLOY_DIR_IPK.rst

   :term:`DEPLOY_DIR_RPM`
      .. include:: variables/DEPLOY_DIR_RPM.rst

   :term:`DEPLOYDIR`
      .. include:: variables/DEPLOYDIR.rst

   :term:`DESCRIPTION`
      .. include:: variables/DESCRIPTION.rst

   :term:`DEV_PKG_DEPENDENCY`
      .. include:: variables/DEV_PKG_DEPENDENCY.rst

   :term:`DISABLE_STATIC`
      .. include:: variables/DISABLE_STATIC.rst

   :term:`DISTRO`
      .. include:: variables/DISTRO.rst

   :term:`DISTRO_CODENAME`
      .. include:: variables/DISTRO_CODENAME.rst

   :term:`DISTRO_EXTRA_RDEPENDS`
      .. include:: variables/DISTRO_EXTRA_RDEPENDS.rst

   :term:`DISTRO_EXTRA_RRECOMMENDS`
      .. include:: variables/DISTRO_EXTRA_RRECOMMENDS.rst

   :term:`DISTRO_FEATURES`
      .. include:: variables/DISTRO_FEATURES.rst

   :term:`DISTRO_FEATURES_DEFAULTS`
      .. include:: variables/DISTRO_FEATURES_DEFAULTS.rst

   :term:`DISTRO_FEATURES_FILTER_NATIVE`
      .. include:: variables/DISTRO_FEATURES_FILTER_NATIVE.rst

   :term:`DISTRO_FEATURES_FILTER_NATIVESDK`
      .. include:: variables/DISTRO_FEATURES_FILTER_NATIVESDK.rst

   :term:`DISTRO_FEATURES_NATIVE`
      .. include:: variables/DISTRO_FEATURES_NATIVE.rst

   :term:`DISTRO_FEATURES_NATIVESDK`
      .. include:: variables/DISTRO_FEATURES_NATIVESDK.rst

   :term:`DISTRO_FEATURES_OPTED_OUT`
      .. include:: variables/DISTRO_FEATURES_OPTED_OUT.rst

   :term:`DISTRO_NAME`
      .. include:: variables/DISTRO_NAME.rst

   :term:`DISTRO_VERSION`
      .. include:: variables/DISTRO_VERSION.rst

   :term:`DISTROOVERRIDES`
      .. include:: variables/DISTROOVERRIDES.rst

   :term:`DL_DIR`
      .. include:: variables/DL_DIR.rst

   :term:`DOC_COMPRESS`
      .. include:: variables/DOC_COMPRESS.rst

   :term:`DT_FILES`
      .. include:: variables/DT_FILES.rst

   :term:`DT_FILES_PATH`
      .. include:: variables/DT_FILES_PATH.rst

   :term:`DT_PADDING_SIZE`
      .. include:: variables/DT_PADDING_SIZE.rst

   :term:`EFI_ARCH`
      .. include:: variables/EFI_ARCH.rst

   :term:`EFI_PROVIDER`
      .. include:: variables/EFI_PROVIDER.rst

   :term:`EFI_UKI_DIR`
      .. include:: variables/EFI_UKI_DIR.rst

   :term:`EFI_UKI_PATH`
      .. include:: variables/EFI_UKI_PATH.rst

   :term:`ENABLE_BINARY_LOCALE_GENERATION`
      .. include:: variables/ENABLE_BINARY_LOCALE_GENERATION.rst

   :term:`ERR_REPORT_DIR`
      .. include:: variables/ERR_REPORT_DIR.rst

   :term:`ERROR_QA`
      .. include:: variables/ERROR_QA.rst

   :term:`ESDK_CLASS_INHERIT_DISABLE`
      .. include:: variables/ESDK_CLASS_INHERIT_DISABLE.rst

   :term:`ESDK_LOCALCONF_ALLOW`
      .. include:: variables/ESDK_LOCALCONF_ALLOW.rst

   :term:`ESDK_LOCALCONF_REMOVE`
      .. include:: variables/ESDK_LOCALCONF_REMOVE.rst

   :term:`EXCLUDE_FROM_SHLIBS`
      .. include:: variables/EXCLUDE_FROM_SHLIBS.rst

   :term:`EXCLUDE_FROM_WORLD`
      .. include:: variables/EXCLUDE_FROM_WORLD.rst

   :term:`EXTENDPE`
      .. include:: variables/EXTENDPE.rst

   :term:`EXTENDPKGV`
      .. include:: variables/EXTENDPKGV.rst

   :term:`EXTERNAL_KERNEL_DEVICETREE`
      .. include:: variables/EXTERNAL_KERNEL_DEVICETREE.rst

   :term:`EXTERNAL_KERNEL_TOOLS`
      .. include:: variables/EXTERNAL_KERNEL_TOOLS.rst

   :term:`EXTERNAL_TOOLCHAIN`
      .. include:: variables/EXTERNAL_TOOLCHAIN.rst

   :term:`EXTERNALSRC`
      .. include:: variables/EXTERNALSRC.rst

   :term:`EXTERNALSRC_BUILD`
      .. include:: variables/EXTERNALSRC_BUILD.rst

   :term:`EXTRA_AUTORECONF`
      .. include:: variables/EXTRA_AUTORECONF.rst

   :term:`EXTRA_IMAGE_FEATURES`
      .. include:: variables/EXTRA_IMAGE_FEATURES.rst

   :term:`EXTRA_IMAGECMD`
      .. include:: variables/EXTRA_IMAGECMD.rst

   :term:`EXTRA_IMAGEDEPENDS`
      .. include:: variables/EXTRA_IMAGEDEPENDS.rst

   :term:`EXTRA_OECMAKE`
      .. include:: variables/EXTRA_OECMAKE.rst

   :term:`EXTRA_OECONF`
      .. include:: variables/EXTRA_OECONF.rst

   :term:`EXTRA_OEMAKE`
      .. include:: variables/EXTRA_OEMAKE.rst

   :term:`EXTRA_OEMESON`
      .. include:: variables/EXTRA_OEMESON.rst

   :term:`EXTRA_OESCONS`
      .. include:: variables/EXTRA_OESCONS.rst

   :term:`EXTRA_USERS_PARAMS`
      .. include:: variables/EXTRA_USERS_PARAMS.rst

   :term:`EXTRANATIVEPATH`
      .. include:: variables/EXTRANATIVEPATH.rst

   :term:`FAKEROOT`
      .. include:: variables/FAKEROOT.rst

   :term:`FAKEROOTBASEENV`
      .. include:: variables/FAKEROOTBASEENV.rst

   :term:`FAKEROOTCMD`
      .. include:: variables/FAKEROOTCMD.rst

   :term:`FAKEROOTDIRS`
      .. include:: variables/FAKEROOTDIRS.rst

   :term:`FAKEROOTENV`
      .. include:: variables/FAKEROOTENV.rst

   :term:`FAKEROOTNOENV`
      .. include:: variables/FAKEROOTNOENV.rst

   :term:`FC`
      .. include:: variables/FC.rst

   :term:`FEATURE_PACKAGES`
      .. include:: variables/FEATURE_PACKAGES.rst

   :term:`FEED_DEPLOYDIR_BASE_URI`
      .. include:: variables/FEED_DEPLOYDIR_BASE_URI.rst

   :term:`FETCHCMD`
      .. include:: variables/FETCHCMD.rst

   :term:`FILE`
      .. include:: variables/FILE.rst

   :term:`FILES`
      .. include:: variables/FILES.rst

   :term:`FILES_SOLIBSDEV`
      .. include:: variables/FILES_SOLIBSDEV.rst

   :term:`FILESEXTRAPATHS`
      .. include:: variables/FILESEXTRAPATHS.rst

   :term:`FILESOVERRIDES`
      .. include:: variables/FILESOVERRIDES.rst

   :term:`FILESPATH`
      .. include:: variables/FILESPATH.rst

   :term:`FILESYSTEM_PERMS_TABLES`
      .. include:: variables/FILESYSTEM_PERMS_TABLES.rst

   :term:`FIRMWARE_COMPRESSION`
      .. include:: variables/FIRMWARE_COMPRESSION.rst

   :term:`FIT_ADDRESS_CELLS`
      .. include:: variables/FIT_ADDRESS_CELLS.rst

   :term:`FIT_CONF_DEFAULT_DTB`
      .. include:: variables/FIT_CONF_DEFAULT_DTB.rst

   :term:`FIT_CONF_MAPPINGS`
      .. include:: variables/FIT_CONF_MAPPINGS.rst

   :term:`FIT_CONF_PREFIX`
      .. include:: variables/FIT_CONF_PREFIX.rst

   :term:`FIT_DESC`
      .. include:: variables/FIT_DESC.rst

   :term:`FIT_GENERATE_KEYS`
      .. include:: variables/FIT_GENERATE_KEYS.rst

   :term:`FIT_HASH_ALG`
      .. include:: variables/FIT_HASH_ALG.rst

   :term:`FIT_KERNEL_COMP_ALG`
      .. include:: variables/FIT_KERNEL_COMP_ALG.rst

   :term:`FIT_KERNEL_COMP_ALG_EXTENSION`
      .. include:: variables/FIT_KERNEL_COMP_ALG_EXTENSION.rst

   :term:`FIT_KERNEL_SIGN_ENABLE`
      .. include:: variables/FIT_KERNEL_SIGN_ENABLE.rst

   :term:`FIT_KERNEL_SIGN_KEYDIR`
      .. include:: variables/FIT_KERNEL_SIGN_KEYDIR.rst

   :term:`FIT_KERNEL_SIGN_KEYNAME`
      .. include:: variables/FIT_KERNEL_SIGN_KEYNAME.rst

   :term:`FIT_KEY_GENRSA_ARGS`
      .. include:: variables/FIT_KEY_GENRSA_ARGS.rst

   :term:`FIT_KEY_REQ_ARGS`
      .. include:: variables/FIT_KEY_REQ_ARGS.rst

   :term:`FIT_KEY_SIGN_PKCS`
      .. include:: variables/FIT_KEY_SIGN_PKCS.rst

   :term:`FIT_LOADABLE_ARCH`
      .. include:: variables/FIT_LOADABLE_ARCH.rst

   :term:`FIT_LOADABLE_COMPRESSION`
      .. include:: variables/FIT_LOADABLE_COMPRESSION.rst

   :term:`FIT_LOADABLE_DESCRIPTION`
      .. include:: variables/FIT_LOADABLE_DESCRIPTION.rst

   :term:`FIT_LOADABLE_ENTRYPOINT`
      .. include:: variables/FIT_LOADABLE_ENTRYPOINT.rst

   :term:`FIT_LOADABLE_FILENAME`
      .. include:: variables/FIT_LOADABLE_FILENAME.rst

   :term:`FIT_LOADABLE_LOADADDRESS`
      .. include:: variables/FIT_LOADABLE_LOADADDRESS.rst

   :term:`FIT_LOADABLE_OS`
      .. include:: variables/FIT_LOADABLE_OS.rst

   :term:`FIT_LOADABLE_TYPE`
      .. include:: variables/FIT_LOADABLE_TYPE.rst

   :term:`FIT_LOADABLES`
      .. include:: variables/FIT_LOADABLES.rst

   :term:`FIT_MKIMAGE_EXTRA_OPTS`
      .. include:: variables/FIT_MKIMAGE_EXTRA_OPTS.rst

   :term:`FIT_PAD_ALG`
      .. include:: variables/FIT_PAD_ALG.rst

   :term:`FIT_SIGN_ALG`
      .. include:: variables/FIT_SIGN_ALG.rst

   :term:`FIT_SIGN_INDIVIDUAL`
      .. include:: variables/FIT_SIGN_INDIVIDUAL.rst

   :term:`FIT_SIGN_NUMBITS`
      .. include:: variables/FIT_SIGN_NUMBITS.rst

   :term:`FIT_UBOOT_ENV`
      .. include:: variables/FIT_UBOOT_ENV.rst

   :term:`FONT_EXTRA_RDEPENDS`
      .. include:: variables/FONT_EXTRA_RDEPENDS.rst

   :term:`FONT_PACKAGES`
      .. include:: variables/FONT_PACKAGES.rst

   :term:`FORCE_RO_REMOVE`
      .. include:: variables/FORCE_RO_REMOVE.rst

   :term:`FULL_OPTIMIZATION`
      .. include:: variables/FULL_OPTIMIZATION.rst

   :term:`GCCPIE`
      .. include:: variables/GCCPIE.rst

   :term:`GCCVERSION`
      .. include:: variables/GCCVERSION.rst

   :term:`GDB`
      .. include:: variables/GDB.rst

   :term:`GIR_EXTRA_LIBS_PATH`
      .. include:: variables/GIR_EXTRA_LIBS_PATH.rst

   :term:`GITDIR`
      .. include:: variables/GITDIR.rst

   :term:`GITHUB_BASE_URI`
      .. include:: variables/GITHUB_BASE_URI.rst

   :term:`GLIBC_GENERATE_LOCALES`
      .. include:: variables/GLIBC_GENERATE_LOCALES.rst

   :term:`GO_IMPORT`
      .. include:: variables/GO_IMPORT.rst

   :term:`GO_INSTALL`
      .. include:: variables/GO_INSTALL.rst

   :term:`GO_INSTALL_FILTEROUT`
      .. include:: variables/GO_INSTALL_FILTEROUT.rst

   :term:`GO_WORKDIR`
      .. include:: variables/GO_WORKDIR.rst

   :term:`GROUPADD_PARAM`
      .. include:: variables/GROUPADD_PARAM.rst

   :term:`GROUPMEMS_PARAM`
      .. include:: variables/GROUPMEMS_PARAM.rst

   :term:`GRUB_GFXSERIAL`
      .. include:: variables/GRUB_GFXSERIAL.rst

   :term:`GRUB_MKIMAGE_OPTS`
      .. include:: variables/GRUB_MKIMAGE_OPTS.rst

   :term:`GRUB_OPTS`
      .. include:: variables/GRUB_OPTS.rst

   :term:`GRUB_TIMEOUT`
      .. include:: variables/GRUB_TIMEOUT.rst

   :term:`GRUB_TITLE`
      .. include:: variables/GRUB_TITLE.rst

   :term:`GTKIMMODULES_PACKAGES`
      .. include:: variables/GTKIMMODULES_PACKAGES.rst

   :term:`HGDIR`
      .. include:: variables/HGDIR.rst

   :term:`HOMEPAGE`
      .. include:: variables/HOMEPAGE.rst

   :term:`HOST_ARCH`
      .. include:: variables/HOST_ARCH.rst

   :term:`HOST_AS_ARCH`
      .. include:: variables/HOST_AS_ARCH.rst

   :term:`HOST_CC_ARCH`
      .. include:: variables/HOST_CC_ARCH.rst

   :term:`HOST_LD_ARCH`
      .. include:: variables/HOST_LD_ARCH.rst

   :term:`HOST_OS`
      .. include:: variables/HOST_OS.rst

   :term:`HOST_PREFIX`
      .. include:: variables/HOST_PREFIX.rst

   :term:`HOST_SYS`
      .. include:: variables/HOST_SYS.rst

   :term:`HOST_VENDOR`
      .. include:: variables/HOST_VENDOR.rst

   :term:`HOSTTOOLS`
      .. include:: variables/HOSTTOOLS.rst

   :term:`HOSTTOOLS_NONFATAL`
      .. include:: variables/HOSTTOOLS_NONFATAL.rst

   :term:`IMAGE_BASENAME`
      .. include:: variables/IMAGE_BASENAME.rst

   :term:`IMAGE_BOOT_FILES`
      .. include:: variables/IMAGE_BOOT_FILES.rst

   :term:`IMAGE_BUILDINFO_FILE`
      .. include:: variables/IMAGE_BUILDINFO_FILE.rst

   :term:`IMAGE_BUILDINFO_VARS`
      .. include:: variables/IMAGE_BUILDINFO_VARS.rst

   :term:`IMAGE_CLASSES`
      .. include:: variables/IMAGE_CLASSES.rst

   :term:`IMAGE_CMD`
      .. include:: variables/IMAGE_CMD.rst

   :term:`IMAGE_CONTAINER_NO_DUMMY`
      .. include:: variables/IMAGE_CONTAINER_NO_DUMMY.rst

   :term:`IMAGE_DEVICE_TABLES`
      .. include:: variables/IMAGE_DEVICE_TABLES.rst

   :term:`IMAGE_EFI_BOOT_FILES`
      .. include:: variables/IMAGE_EFI_BOOT_FILES.rst

   :term:`IMAGE_EXTRA_PARTITION_FILES`
      .. include:: variables/IMAGE_EXTRA_PARTITION_FILES.rst

   :term:`IMAGE_FEATURES`
      .. include:: variables/IMAGE_FEATURES.rst

   :term:`IMAGE_FSTYPES`
      .. include:: variables/IMAGE_FSTYPES.rst

   :term:`IMAGE_FSTYPES_DEBUGFS`
      .. include:: variables/IMAGE_FSTYPES_DEBUGFS.rst

   :term:`IMAGE_GEN_DEBUGFS`
      .. include:: variables/IMAGE_GEN_DEBUGFS.rst

   :term:`IMAGE_INSTALL`
      .. include:: variables/IMAGE_INSTALL.rst

   :term:`IMAGE_LINGUAS`
      .. include:: variables/IMAGE_LINGUAS.rst

   :term:`IMAGE_LINK_NAME`
      .. include:: variables/IMAGE_LINK_NAME.rst

   :term:`IMAGE_MACHINE_SUFFIX`
      .. include:: variables/IMAGE_MACHINE_SUFFIX.rst

   :term:`IMAGE_MANIFEST`
      .. include:: variables/IMAGE_MANIFEST.rst

   :term:`IMAGE_NAME`
      .. include:: variables/IMAGE_NAME.rst

   :term:`IMAGE_NAME_SUFFIX`
      .. include:: variables/IMAGE_NAME_SUFFIX.rst

   :term:`IMAGE_OUTPUT_MANIFEST`
      .. include:: variables/IMAGE_OUTPUT_MANIFEST.rst

   :term:`IMAGE_OUTPUT_MANIFEST_DIR`
      .. include:: variables/IMAGE_OUTPUT_MANIFEST_DIR.rst

   :term:`IMAGE_OVERHEAD_FACTOR`
      .. include:: variables/IMAGE_OVERHEAD_FACTOR.rst

   :term:`IMAGE_PKGTYPE`
      .. include:: variables/IMAGE_PKGTYPE.rst

   :term:`IMAGE_POSTPROCESS_COMMAND`
      .. include:: variables/IMAGE_POSTPROCESS_COMMAND.rst

   :term:`IMAGE_PREPROCESS_COMMAND`
      .. include:: variables/IMAGE_PREPROCESS_COMMAND.rst

   :term:`IMAGE_ROOTFS`
      .. include:: variables/IMAGE_ROOTFS.rst

   :term:`IMAGE_ROOTFS_ALIGNMENT`
      .. include:: variables/IMAGE_ROOTFS_ALIGNMENT.rst

   :term:`IMAGE_ROOTFS_EXTRA_SPACE`
      .. include:: variables/IMAGE_ROOTFS_EXTRA_SPACE.rst

   :term:`IMAGE_ROOTFS_MAXSIZE`
      .. include:: variables/IMAGE_ROOTFS_MAXSIZE.rst

   :term:`IMAGE_ROOTFS_SIZE`
      .. include:: variables/IMAGE_ROOTFS_SIZE.rst

   :term:`IMAGE_TYPEDEP`
      .. include:: variables/IMAGE_TYPEDEP.rst

   :term:`IMAGE_TYPES`
      .. include:: variables/IMAGE_TYPES.rst

   :term:`IMAGE_VERSION_SUFFIX`
      .. include:: variables/IMAGE_VERSION_SUFFIX.rst

   :term:`IMGDEPLOYDIR`
      .. include:: variables/IMGDEPLOYDIR.rst

   :term:`IMGMANIFESTDIR`
      .. include:: variables/IMGMANIFESTDIR.rst

   :term:`INCOMPATIBLE_LICENSE`
      .. include:: variables/INCOMPATIBLE_LICENSE.rst

   :term:`INCOMPATIBLE_LICENSE_EXCEPTIONS`
      .. include:: variables/INCOMPATIBLE_LICENSE_EXCEPTIONS.rst

   :term:`INHERIT`
      .. include:: variables/INHERIT.rst

   :term:`INHERIT_DISTRO`
      .. include:: variables/INHERIT_DISTRO.rst

   :term:`INHIBIT_AUTOTOOLS_DEPS`
      .. include:: variables/INHIBIT_AUTOTOOLS_DEPS.rst

   :term:`INHIBIT_DEFAULT_DEPS`
      .. include:: variables/INHIBIT_DEFAULT_DEPS.rst

   :term:`INHIBIT_DEFAULT_RUST_DEPS`
      .. include:: variables/INHIBIT_DEFAULT_RUST_DEPS.rst

   :term:`INHIBIT_PACKAGE_DEBUG_SPLIT`
      .. include:: variables/INHIBIT_PACKAGE_DEBUG_SPLIT.rst

   :term:`INHIBIT_PACKAGE_STRIP`
      .. include:: variables/INHIBIT_PACKAGE_STRIP.rst

   :term:`INHIBIT_SYSROOT_STRIP`
      .. include:: variables/INHIBIT_SYSROOT_STRIP.rst

   :term:`INHIBIT_UPDATERCD_BBCLASS`
      .. include:: variables/INHIBIT_UPDATERCD_BBCLASS.rst

   :term:`INIT_MANAGER`
      .. include:: variables/INIT_MANAGER.rst

   :term:`INITRAMFS_DEPLOY_DIR_IMAGE`
      .. include:: variables/INITRAMFS_DEPLOY_DIR_IMAGE.rst

   :term:`INITRAMFS_FSTYPES`
      .. include:: variables/INITRAMFS_FSTYPES.rst

   :term:`INITRAMFS_IMAGE`
      .. include:: variables/INITRAMFS_IMAGE.rst

   :term:`INITRAMFS_IMAGE_BUNDLE`
      .. include:: variables/INITRAMFS_IMAGE_BUNDLE.rst

   :term:`INITRAMFS_IMAGE_NAME`
      .. include:: variables/INITRAMFS_IMAGE_NAME.rst

   :term:`INITRAMFS_LINK_NAME`
      .. include:: variables/INITRAMFS_LINK_NAME.rst

   :term:`INITRAMFS_MAXSIZE`
      .. include:: variables/INITRAMFS_MAXSIZE.rst

   :term:`INITRAMFS_MULTICONFIG`
      .. include:: variables/INITRAMFS_MULTICONFIG.rst

   :term:`INITRAMFS_NAME`
      .. include:: variables/INITRAMFS_NAME.rst

   :term:`INITRD`
      .. include:: variables/INITRD.rst

   :term:`INITRD_IMAGE`
      .. include:: variables/INITRD_IMAGE.rst

   :term:`INITSCRIPT_NAME`
      .. include:: variables/INITSCRIPT_NAME.rst

   :term:`INITSCRIPT_PACKAGES`
      .. include:: variables/INITSCRIPT_PACKAGES.rst

   :term:`INITSCRIPT_PARAMS`
      .. include:: variables/INITSCRIPT_PARAMS.rst

   :term:`INSANE_SKIP`
      .. include:: variables/INSANE_SKIP.rst

   :term:`INSTALL_TIMEZONE_FILE`
      .. include:: variables/INSTALL_TIMEZONE_FILE.rst

   :term:`IPK_FEED_URIS`
      .. include:: variables/IPK_FEED_URIS.rst

   :term:`KARCH`
      .. include:: variables/KARCH.rst

   :term:`KBRANCH`
      .. include:: variables/KBRANCH.rst

   :term:`KBUILD_DEFCONFIG`
      .. include:: variables/KBUILD_DEFCONFIG.rst

   :term:`KCONF_AUDIT_LEVEL`
      .. include:: variables/KCONF_AUDIT_LEVEL.rst

   :term:`KCONF_BSP_AUDIT_LEVEL`
      .. include:: variables/KCONF_BSP_AUDIT_LEVEL.rst

   :term:`KCONFIG_CONFIG_ROOTDIR`
      .. include:: variables/KCONFIG_CONFIG_ROOTDIR.rst

   :term:`KCONFIG_MODE`
      .. include:: variables/KCONFIG_MODE.rst

   :term:`KERNEL_ALT_IMAGETYPE`
      .. include:: variables/KERNEL_ALT_IMAGETYPE.rst

   :term:`KERNEL_ARTIFACT_NAME`
      .. include:: variables/KERNEL_ARTIFACT_NAME.rst

   :term:`KERNEL_CLASSES`
      .. include:: variables/KERNEL_CLASSES.rst

   :term:`KERNEL_CONSOLE`
      .. include:: variables/KERNEL_CONSOLE.rst

   :term:`KERNEL_DANGLING_FEATURES_WARN_ONLY`
      .. include:: variables/KERNEL_DANGLING_FEATURES_WARN_ONLY.rst

   :term:`KERNEL_DEBUG_TIMESTAMPS`
      .. include:: variables/KERNEL_DEBUG_TIMESTAMPS.rst

   :term:`KERNEL_DEPLOY_DEPEND`
      .. include:: variables/KERNEL_DEPLOY_DEPEND.rst

   :term:`KERNEL_DEVICETREE`
      .. include:: variables/KERNEL_DEVICETREE.rst

   :term:`KERNEL_DEVICETREE_BUNDLE`
      .. include:: variables/KERNEL_DEVICETREE_BUNDLE.rst

   :term:`KERNEL_DTB_LINK_NAME`
      .. include:: variables/KERNEL_DTB_LINK_NAME.rst

   :term:`KERNEL_DTB_NAME`
      .. include:: variables/KERNEL_DTB_NAME.rst

   :term:`KERNEL_DTBDEST`
      .. include:: variables/KERNEL_DTBDEST.rst

   :term:`KERNEL_DTBVENDORED`
      .. include:: variables/KERNEL_DTBVENDORED.rst

   :term:`KERNEL_DTC_FLAGS`
      .. include:: variables/KERNEL_DTC_FLAGS.rst

   :term:`KERNEL_EXTRA_ARGS`
      .. include:: variables/KERNEL_EXTRA_ARGS.rst

   :term:`KERNEL_FEATURES`
      .. include:: variables/KERNEL_FEATURES.rst

   :term:`KERNEL_FIT_LINK_NAME`
      .. include:: variables/KERNEL_FIT_LINK_NAME.rst

   :term:`KERNEL_FIT_NAME`
      .. include:: variables/KERNEL_FIT_NAME.rst

   :term:`KERNEL_IMAGE_LINK_NAME`
      .. include:: variables/KERNEL_IMAGE_LINK_NAME.rst

   :term:`KERNEL_IMAGE_MAXSIZE`
      .. include:: variables/KERNEL_IMAGE_MAXSIZE.rst

   :term:`KERNEL_IMAGE_NAME`
      .. include:: variables/KERNEL_IMAGE_NAME.rst

   :term:`KERNEL_IMAGETYPE`
      .. include:: variables/KERNEL_IMAGETYPE.rst

   :term:`KERNEL_IMAGETYPES`
      .. include:: variables/KERNEL_IMAGETYPES.rst

   :term:`KERNEL_LOCALVERSION`
      .. include:: variables/KERNEL_LOCALVERSION.rst

   :term:`KERNEL_MODULE_AUTOLOAD`
      .. include:: variables/KERNEL_MODULE_AUTOLOAD.rst

   :term:`KERNEL_MODULE_PROBECONF`
      .. include:: variables/KERNEL_MODULE_PROBECONF.rst

   :term:`KERNEL_PACKAGE_NAME`
      .. include:: variables/KERNEL_PACKAGE_NAME.rst

   :term:`KERNEL_PATH`
      .. include:: variables/KERNEL_PATH.rst

   :term:`KERNEL_SPLIT_MODULES`
      .. include:: variables/KERNEL_SPLIT_MODULES.rst

   :term:`KERNEL_SRC`
      .. include:: variables/KERNEL_SRC.rst

   :term:`KERNEL_STRIP`
      .. include:: variables/KERNEL_STRIP.rst

   :term:`KERNEL_VERSION`
      .. include:: variables/KERNEL_VERSION.rst

   :term:`KERNELDEPMODDEPEND`
      .. include:: variables/KERNELDEPMODDEPEND.rst

   :term:`KFEATURE_DESCRIPTION`
      .. include:: variables/KFEATURE_DESCRIPTION.rst

   :term:`KMACHINE`
      .. include:: variables/KMACHINE.rst

   :term:`KMETA_AUDIT`
      .. include:: variables/KMETA_AUDIT.rst

   :term:`KMETA_AUDIT_WERROR`
      .. include:: variables/KMETA_AUDIT_WERROR.rst

   :term:`KMETA_CONFIG_FEATURES`
      .. include:: variables/KMETA_CONFIG_FEATURES.rst

   :term:`KTYPE`
      .. include:: variables/KTYPE.rst

   :term:`LABELS`
      .. include:: variables/LABELS.rst

   :term:`LAYERDEPENDS`
      .. include:: variables/LAYERDEPENDS.rst

   :term:`LAYERDIR`
      .. include:: variables/LAYERDIR.rst

   :term:`LAYERDIR_RE`
      .. include:: variables/LAYERDIR_RE.rst

   :term:`LAYERRECOMMENDS`
      .. include:: variables/LAYERRECOMMENDS.rst

   :term:`LAYERSERIES_COMPAT`
      .. include:: variables/LAYERSERIES_COMPAT.rst

   :term:`LAYERVERSION`
      .. include:: variables/LAYERVERSION.rst

   :term:`LD`
      .. include:: variables/LD.rst

   :term:`LDFLAGS`
      .. include:: variables/LDFLAGS.rst

   :term:`LEAD_SONAME`
      .. include:: variables/LEAD_SONAME.rst

   :term:`LIC_FILES_CHKSUM`
      .. include:: variables/LIC_FILES_CHKSUM.rst

   :term:`LICENSE`
      .. include:: variables/LICENSE.rst

   :term:`LICENSE_CREATE_PACKAGE`
      .. include:: variables/LICENSE_CREATE_PACKAGE.rst

   :term:`LICENSE_FLAGS`
      .. include:: variables/LICENSE_FLAGS.rst

   :term:`LICENSE_FLAGS_ACCEPTED`
      .. include:: variables/LICENSE_FLAGS_ACCEPTED.rst

   :term:`LICENSE_FLAGS_DETAILS`
      .. include:: variables/LICENSE_FLAGS_DETAILS.rst

   :term:`LICENSE_PATH`
      .. include:: variables/LICENSE_PATH.rst

   :term:`LINUX_KERNEL_TYPE`
      .. include:: variables/LINUX_KERNEL_TYPE.rst

   :term:`LINUX_VERSION`
      .. include:: variables/LINUX_VERSION.rst

   :term:`LINUX_VERSION_EXTENSION`
      .. include:: variables/LINUX_VERSION_EXTENSION.rst

   :term:`LOCALE_PATHS`
      .. include:: variables/LOCALE_PATHS.rst

   :term:`LOCALE_UTF8_IS_DEFAULT`
      .. include:: variables/LOCALE_UTF8_IS_DEFAULT.rst

   :term:`LOG_DIR`
      .. include:: variables/LOG_DIR.rst

   :term:`LTO`
      .. include:: variables/LTO.rst

   :term:`MACHINE`
      .. include:: variables/MACHINE.rst

   :term:`MACHINE_ARCH`
      .. include:: variables/MACHINE_ARCH.rst

   :term:`MACHINE_ESSENTIAL_EXTRA_RDEPENDS`
      .. include:: variables/MACHINE_ESSENTIAL_EXTRA_RDEPENDS.rst

   :term:`MACHINE_ESSENTIAL_EXTRA_RRECOMMENDS`
      .. include:: variables/MACHINE_ESSENTIAL_EXTRA_RRECOMMENDS.rst

   :term:`MACHINE_EXTRA_RDEPENDS`
      .. include:: variables/MACHINE_EXTRA_RDEPENDS.rst

   :term:`MACHINE_EXTRA_RRECOMMENDS`
      .. include:: variables/MACHINE_EXTRA_RRECOMMENDS.rst

   :term:`MACHINE_FEATURES`
      .. include:: variables/MACHINE_FEATURES.rst

   :term:`MACHINE_FEATURES_DEFAULTS`
      .. include:: variables/MACHINE_FEATURES_DEFAULTS.rst

   :term:`MACHINE_FEATURES_OPTED_OUT`
      .. include:: variables/MACHINE_FEATURES_OPTED_OUT.rst

   :term:`MACHINEOVERRIDES`
      .. include:: variables/MACHINEOVERRIDES.rst

   :term:`MAINTAINER`
      .. include:: variables/MAINTAINER.rst

   :term:`MESON_BUILDTYPE`
      .. include:: variables/MESON_BUILDTYPE.rst

   :term:`MESON_INSTALL_TAGS`
      .. include:: variables/MESON_INSTALL_TAGS.rst

   :term:`MESON_TARGET`
      .. include:: variables/MESON_TARGET.rst

   :term:`METADATA_BRANCH`
      .. include:: variables/METADATA_BRANCH.rst

   :term:`METADATA_REVISION`
      .. include:: variables/METADATA_REVISION.rst

   :term:`MIME_XDG_PACKAGES`
      .. include:: variables/MIME_XDG_PACKAGES.rst

   :term:`MIRRORS`
      .. include:: variables/MIRRORS.rst

   :term:`MLPREFIX`
      .. include:: variables/MLPREFIX.rst

   :term:`module_autoload`
      .. include:: variables/module_autoload.rst

   :term:`module_conf`
      .. include:: variables/module_conf.rst

   :term:`MODULE_TARBALL_DEPLOY`
      .. include:: variables/MODULE_TARBALL_DEPLOY.rst

   :term:`MODULE_TARBALL_LINK_NAME`
      .. include:: variables/MODULE_TARBALL_LINK_NAME.rst

   :term:`MODULE_TARBALL_NAME`
      .. include:: variables/MODULE_TARBALL_NAME.rst

   :term:`MOUNT_BASE`
      .. include:: variables/MOUNT_BASE.rst

   :term:`MOUNT_GROUP`
      .. include:: variables/MOUNT_GROUP.rst

   :term:`MULTIMACH_TARGET_SYS`
      .. include:: variables/MULTIMACH_TARGET_SYS.rst

   :term:`NATIVELSBSTRING`
      .. include:: variables/NATIVELSBSTRING.rst

   :term:`NM`
      .. include:: variables/NM.rst

   :term:`NO_GENERIC_LICENSE`
      .. include:: variables/NO_GENERIC_LICENSE.rst

   :term:`NO_RECOMMENDATIONS`
      .. include:: variables/NO_RECOMMENDATIONS.rst

   :term:`NOAUTOPACKAGEDEBUG`
      .. include:: variables/NOAUTOPACKAGEDEBUG.rst

   :term:`NON_MULTILIB_RECIPES`
      .. include:: variables/NON_MULTILIB_RECIPES.rst

   :term:`OBJCOPY`
      .. include:: variables/OBJCOPY.rst

   :term:`OBJDUMP`
      .. include:: variables/OBJDUMP.rst

   :term:`OE_BINCONFIG_EXTRA_MANGLE`
      .. include:: variables/OE_BINCONFIG_EXTRA_MANGLE.rst

   :term:`OE_FRAGMENTS`
      .. include:: variables/OE_FRAGMENTS.rst

   :term:`OE_FRAGMENTS_BUILTIN`
      .. include:: variables/OE_FRAGMENTS_BUILTIN.rst

   :term:`OE_FRAGMENTS_METADATA_VARS`
      .. include:: variables/OE_FRAGMENTS_METADATA_VARS.rst

   :term:`OE_FRAGMENTS_PREFIX`
      .. include:: variables/OE_FRAGMENTS_PREFIX.rst

   :term:`OE_INIT_ENV_SCRIPT`
      .. include:: variables/OE_INIT_ENV_SCRIPT.rst

   :term:`OE_SHARED_UMASK`
      .. include:: variables/OE_SHARED_UMASK.rst

   :term:`OE_TERMINAL`
      .. include:: variables/OE_TERMINAL.rst

   :term:`OECMAKE_GENERATOR`
      .. include:: variables/OECMAKE_GENERATOR.rst

   :term:`OEQA_REPRODUCIBLE_TEST_LEAF_TARGETS`
      .. include:: variables/OEQA_REPRODUCIBLE_TEST_LEAF_TARGETS.rst

   :term:`OEQA_REPRODUCIBLE_TEST_PACKAGE`
      .. include:: variables/OEQA_REPRODUCIBLE_TEST_PACKAGE.rst

   :term:`OEQA_REPRODUCIBLE_TEST_SSTATE_TARGETS`
      .. include:: variables/OEQA_REPRODUCIBLE_TEST_SSTATE_TARGETS.rst

   :term:`OEQA_REPRODUCIBLE_TEST_TARGET`
      .. include:: variables/OEQA_REPRODUCIBLE_TEST_TARGET.rst

   :term:`OEROOT`
      .. include:: variables/OEROOT.rst

   :term:`OLDEST_KERNEL`
      .. include:: variables/OLDEST_KERNEL.rst

   :term:`OPENSSH_HOST_KEY_DIR`
      .. include:: variables/OPENSSH_HOST_KEY_DIR.rst

   :term:`OPENSSH_HOST_KEY_DIR_READONLY_CONFIG`
      .. include:: variables/OPENSSH_HOST_KEY_DIR_READONLY_CONFIG.rst

   :term:`OPKG_MAKE_INDEX_EXTRA_PARAMS`
      .. include:: variables/OPKG_MAKE_INDEX_EXTRA_PARAMS.rst

   :term:`OPKGBUILDCMD`
      .. include:: variables/OPKGBUILDCMD.rst

   :term:`OVERLAYFS_ETC_DEVICE`
      .. include:: variables/OVERLAYFS_ETC_DEVICE.rst

   :term:`OVERLAYFS_ETC_EXPOSE_LOWER`
      .. include:: variables/OVERLAYFS_ETC_EXPOSE_LOWER.rst

   :term:`OVERLAYFS_ETC_FSTYPE`
      .. include:: variables/OVERLAYFS_ETC_FSTYPE.rst

   :term:`OVERLAYFS_ETC_MOUNT_OPTIONS`
      .. include:: variables/OVERLAYFS_ETC_MOUNT_OPTIONS.rst

   :term:`OVERLAYFS_ETC_MOUNT_POINT`
      .. include:: variables/OVERLAYFS_ETC_MOUNT_POINT.rst

   :term:`OVERLAYFS_ETC_USE_ORIG_INIT_NAME`
      .. include:: variables/OVERLAYFS_ETC_USE_ORIG_INIT_NAME.rst

   :term:`OVERLAYFS_MOUNT_POINT`
      .. include:: variables/OVERLAYFS_MOUNT_POINT.rst

   :term:`OVERLAYFS_QA_SKIP`
      .. include:: variables/OVERLAYFS_QA_SKIP.rst

   :term:`OVERLAYFS_WRITABLE_PATHS`
      .. include:: variables/OVERLAYFS_WRITABLE_PATHS.rst

   :term:`OVERRIDES`
      .. include:: variables/OVERRIDES.rst

   :term:`P`
      .. include:: variables/P.rst

   :term:`P4DIR`
      .. include:: variables/P4DIR.rst

   :term:`PACKAGE_ADD_METADATA`
      .. include:: variables/PACKAGE_ADD_METADATA.rst

   :term:`PACKAGE_ARCH`
      .. include:: variables/PACKAGE_ARCH.rst

   :term:`PACKAGE_ARCHS`
      .. include:: variables/PACKAGE_ARCHS.rst

   :term:`PACKAGE_BEFORE_PN`
      .. include:: variables/PACKAGE_BEFORE_PN.rst

   :term:`PACKAGE_CLASSES`
      .. include:: variables/PACKAGE_CLASSES.rst

   :term:`PACKAGE_DEBUG_SPLIT_STYLE`
      .. include:: variables/PACKAGE_DEBUG_SPLIT_STYLE.rst

   :term:`PACKAGE_EXCLUDE`
      .. include:: variables/PACKAGE_EXCLUDE.rst

   :term:`PACKAGE_EXCLUDE_COMPLEMENTARY`
      .. include:: variables/PACKAGE_EXCLUDE_COMPLEMENTARY.rst

   :term:`PACKAGE_EXTRA_ARCHS`
      .. include:: variables/PACKAGE_EXTRA_ARCHS.rst

   :term:`PACKAGE_FEED_ARCHS`
      .. include:: variables/PACKAGE_FEED_ARCHS.rst

   :term:`PACKAGE_FEED_BASE_PATHS`
      .. include:: variables/PACKAGE_FEED_BASE_PATHS.rst

   :term:`PACKAGE_FEED_URIS`
      .. include:: variables/PACKAGE_FEED_URIS.rst

   :term:`PACKAGE_INSTALL`
      .. include:: variables/PACKAGE_INSTALL.rst

   :term:`PACKAGE_INSTALL_ATTEMPTONLY`
      .. include:: variables/PACKAGE_INSTALL_ATTEMPTONLY.rst

   :term:`PACKAGE_PREPROCESS_FUNCS`
      .. include:: variables/PACKAGE_PREPROCESS_FUNCS.rst

   :term:`PACKAGE_WRITE_DEPS`
      .. include:: variables/PACKAGE_WRITE_DEPS.rst

   :term:`PACKAGECONFIG`
      .. include:: variables/PACKAGECONFIG.rst

   :term:`PACKAGECONFIG_CONFARGS`
      .. include:: variables/PACKAGECONFIG_CONFARGS.rst

   :term:`PACKAGEGROUP_DISABLE_COMPLEMENTARY`
      .. include:: variables/PACKAGEGROUP_DISABLE_COMPLEMENTARY.rst

   :term:`PACKAGES`
      .. include:: variables/PACKAGES.rst

   :term:`PACKAGES_DYNAMIC`
      .. include:: variables/PACKAGES_DYNAMIC.rst

   :term:`PACKAGESPLITFUNCS`
      .. include:: variables/PACKAGESPLITFUNCS.rst

   :term:`PARALLEL_MAKE`
      .. include:: variables/PARALLEL_MAKE.rst

   :term:`PARALLEL_MAKEINST`
      .. include:: variables/PARALLEL_MAKEINST.rst

   :term:`PATCHRESOLVE`
      .. include:: variables/PATCHRESOLVE.rst

   :term:`PATCHTOOL`
      .. include:: variables/PATCHTOOL.rst

   :term:`PE`
      .. include:: variables/PE.rst

   :term:`PEP517_WHEEL_PATH`
      .. include:: variables/PEP517_WHEEL_PATH.rst

   :term:`PERSISTENT_DIR`
      .. include:: variables/PERSISTENT_DIR.rst

   :term:`PF`
      .. include:: variables/PF.rst

   :term:`PIXBUF_PACKAGES`
      .. include:: variables/PIXBUF_PACKAGES.rst

   :term:`PKG`
      .. include:: variables/PKG.rst

   :term:`PKG_CONFIG_PATH`
      .. include:: variables/PKG_CONFIG_PATH.rst

   :term:`PKGD`
      .. include:: variables/PKGD.rst

   :term:`PKGDATA_DIR`
      .. include:: variables/PKGDATA_DIR.rst

   :term:`PKGDEST`
      .. include:: variables/PKGDEST.rst

   :term:`PKGDESTWORK`
      .. include:: variables/PKGDESTWORK.rst

   :term:`PKGE`
      .. include:: variables/PKGE.rst

   :term:`PKGR`
      .. include:: variables/PKGR.rst

   :term:`PKGV`
      .. include:: variables/PKGV.rst

   :term:`PN`
      .. include:: variables/PN.rst

   :term:`POPULATE_SDK_POST_HOST_COMMAND`
      .. include:: variables/POPULATE_SDK_POST_HOST_COMMAND.rst

   :term:`POPULATE_SDK_POST_TARGET_COMMAND`
      .. include:: variables/POPULATE_SDK_POST_TARGET_COMMAND.rst

   :term:`PR`
      .. include:: variables/PR.rst

   :term:`PREFERRED_PROVIDER`
      .. include:: variables/PREFERRED_PROVIDER.rst

   :term:`PREFERRED_PROVIDERS`
      .. include:: variables/PREFERRED_PROVIDERS.rst

   :term:`PREFERRED_RPROVIDER`
      .. include:: variables/PREFERRED_RPROVIDER.rst

   :term:`PREFERRED_TOOLCHAIN`
      .. include:: variables/PREFERRED_TOOLCHAIN.rst

   :term:`PREFERRED_TOOLCHAIN_NATIVE`
      .. include:: variables/PREFERRED_TOOLCHAIN_NATIVE.rst

   :term:`PREFERRED_TOOLCHAIN_SDK`
      .. include:: variables/PREFERRED_TOOLCHAIN_SDK.rst

   :term:`PREFERRED_TOOLCHAIN_TARGET`
      .. include:: variables/PREFERRED_TOOLCHAIN_TARGET.rst

   :term:`PREFERRED_VERSION`
      .. include:: variables/PREFERRED_VERSION.rst

   :term:`PREMIRRORS`
      .. include:: variables/PREMIRRORS.rst

   :term:`PRIORITY`
      .. include:: variables/PRIORITY.rst

   :term:`PRIVATE_LIBS`
      .. include:: variables/PRIVATE_LIBS.rst

   :term:`PROVIDES`
      .. include:: variables/PROVIDES.rst

   :term:`PRSERV_HOST`
      .. include:: variables/PRSERV_HOST.rst

   :term:`PRSERV_UPSTREAM`
      .. include:: variables/PRSERV_UPSTREAM.rst

   :term:`PSEUDO_IGNORE_PATHS`
      .. include:: variables/PSEUDO_IGNORE_PATHS.rst

   :term:`PSEUDO_INCLUDE_PATHS`
      .. include:: variables/PSEUDO_INCLUDE_PATHS.rst

   :term:`PTEST_ENABLED`
      .. include:: variables/PTEST_ENABLED.rst

   :term:`PTEST_PYTEST_DIR`
      .. include:: variables/PTEST_PYTEST_DIR.rst

   :term:`PV`
      .. include:: variables/PV.rst

   :term:`PYPI_PACKAGE`
      .. include:: variables/PYPI_PACKAGE.rst

   :term:`PYPI_PACKAGE_EXT`
      .. include:: variables/PYPI_PACKAGE_EXT.rst

   :term:`PYPI_SRC_URI`
      .. include:: variables/PYPI_SRC_URI.rst

   :term:`PYTHON_ABI`
      .. include:: variables/PYTHON_ABI.rst

   :term:`QA_EMPTY_DIRS`
      .. include:: variables/QA_EMPTY_DIRS.rst

   :term:`QA_EMPTY_DIRS_RECOMMENDATION`
      .. include:: variables/QA_EMPTY_DIRS_RECOMMENDATION.rst

   :term:`QB_CMDLINE_IP_SLIRP`
      .. include:: variables/QB_CMDLINE_IP_SLIRP.rst

   :term:`QB_CMDLINE_IP_TAP`
      .. include:: variables/QB_CMDLINE_IP_TAP.rst

   :term:`QB_DEFAULT_FSTYPE`
      .. include:: variables/QB_DEFAULT_FSTYPE.rst

   :term:`QB_DEFAULT_KERNEL`
      .. include:: variables/QB_DEFAULT_KERNEL.rst

   :term:`QB_DRIVE_TYPE`
      .. include:: variables/QB_DRIVE_TYPE.rst

   :term:`QB_GRAPHICS`
      .. include:: variables/QB_GRAPHICS.rst

   :term:`QB_KERNEL_CMDLINE_APPEND`
      .. include:: variables/QB_KERNEL_CMDLINE_APPEND.rst

   :term:`QB_MEM`
      .. include:: variables/QB_MEM.rst

   :term:`QB_NETWORK_DEVICE`
      .. include:: variables/QB_NETWORK_DEVICE.rst

   :term:`QB_NFSROOTFS_EXTRA_OPT`
      .. include:: variables/QB_NFSROOTFS_EXTRA_OPT.rst

   :term:`QB_OPT_APPEND`
      .. include:: variables/QB_OPT_APPEND.rst

   :term:`QB_RNG`
      .. include:: variables/QB_RNG.rst

   :term:`QB_ROOTFS_EXTRA_OPT`
      .. include:: variables/QB_ROOTFS_EXTRA_OPT.rst

   :term:`QB_SERIAL_OPT`
      .. include:: variables/QB_SERIAL_OPT.rst

   :term:`QB_SMP`
      .. include:: variables/QB_SMP.rst

   :term:`QB_TAP_NAMESERVER`
      .. include:: variables/QB_TAP_NAMESERVER.rst

   :term:`QB_TAP_OPT`
      .. include:: variables/QB_TAP_OPT.rst

   :term:`RANLIB`
      .. include:: variables/RANLIB.rst

   :term:`RCONFLICTS`
      .. include:: variables/RCONFLICTS.rst

   :term:`RDEPENDS`
      .. include:: variables/RDEPENDS.rst

   :term:`READELF`
      .. include:: variables/READELF.rst

   :term:`RECIPE_MAINTAINER`
      .. include:: variables/RECIPE_MAINTAINER.rst

   :term:`RECIPE_NO_UPDATE_REASON`
      .. include:: variables/RECIPE_NO_UPDATE_REASON.rst

   :term:`RECIPE_SYSROOT`
      .. include:: variables/RECIPE_SYSROOT.rst

   :term:`RECIPE_SYSROOT_NATIVE`
      .. include:: variables/RECIPE_SYSROOT_NATIVE.rst

   :term:`RECIPE_UPGRADE_EXTRA_TASKS`
      .. include:: variables/RECIPE_UPGRADE_EXTRA_TASKS.rst

   :term:`REPODIR`
      .. include:: variables/REPODIR.rst

   :term:`REQUIRED_COMBINED_FEATURES`
      .. include:: variables/REQUIRED_COMBINED_FEATURES.rst

   :term:`REQUIRED_DISTRO_FEATURES`
      .. include:: variables/REQUIRED_DISTRO_FEATURES.rst

   :term:`REQUIRED_IMAGE_FEATURES`
      .. include:: variables/REQUIRED_IMAGE_FEATURES.rst

   :term:`REQUIRED_MACHINE_FEATURES`
      .. include:: variables/REQUIRED_MACHINE_FEATURES.rst

   :term:`REQUIRED_TUNE_FEATURES`
      .. include:: variables/REQUIRED_TUNE_FEATURES.rst

   :term:`REQUIRED_VERSION`
      .. include:: variables/REQUIRED_VERSION.rst

   :term:`RETAIN_DIRS_ALWAYS`
      .. include:: variables/RETAIN_DIRS_ALWAYS.rst

   :term:`RETAIN_DIRS_FAILURE`
      .. include:: variables/RETAIN_DIRS_FAILURE.rst

   :term:`RETAIN_DIRS_GLOBAL_ALWAYS`
      .. include:: variables/RETAIN_DIRS_GLOBAL_ALWAYS.rst

   :term:`RETAIN_DIRS_GLOBAL_FAILURE`
      .. include:: variables/RETAIN_DIRS_GLOBAL_FAILURE.rst

   :term:`RETAIN_ENABLED`
      .. include:: variables/RETAIN_ENABLED.rst

   :term:`RETAIN_OUTDIR`
      .. include:: variables/RETAIN_OUTDIR.rst

   :term:`RETAIN_TARBALL_SUFFIX`
      .. include:: variables/RETAIN_TARBALL_SUFFIX.rst

   :term:`RM_WORK_EXCLUDE`
      .. include:: variables/RM_WORK_EXCLUDE.rst

   :term:`RM_WORK_EXCLUDE_ITEMS`
      .. include:: variables/RM_WORK_EXCLUDE_ITEMS.rst

   :term:`ROOT_HOME`
      .. include:: variables/ROOT_HOME.rst

   :term:`ROOTFS`
      .. include:: variables/ROOTFS.rst

   :term:`ROOTFS_POSTINSTALL_COMMAND`
      .. include:: variables/ROOTFS_POSTINSTALL_COMMAND.rst

   :term:`ROOTFS_POSTPROCESS_COMMAND`
      .. include:: variables/ROOTFS_POSTPROCESS_COMMAND.rst

   :term:`ROOTFS_POSTUNINSTALL_COMMAND`
      .. include:: variables/ROOTFS_POSTUNINSTALL_COMMAND.rst

   :term:`ROOTFS_PREPROCESS_COMMAND`
      .. include:: variables/ROOTFS_PREPROCESS_COMMAND.rst

   :term:`RPMBUILD_EXTRA_PARAMS`
      .. include:: variables/RPMBUILD_EXTRA_PARAMS.rst

   :term:`RPROVIDES`
      .. include:: variables/RPROVIDES.rst

   :term:`RRECOMMENDS`
      .. include:: variables/RRECOMMENDS.rst

   :term:`RREPLACES`
      .. include:: variables/RREPLACES.rst

   :term:`RSUGGESTS`
      .. include:: variables/RSUGGESTS.rst

   :term:`RUST_CHANNEL`
      .. include:: variables/RUST_CHANNEL.rst

   :term:`S`
      .. include:: variables/S.rst

   :term:`SANITY_REQUIRED_UTILITIES`
      .. include:: variables/SANITY_REQUIRED_UTILITIES.rst

   :term:`SANITY_TESTED_DISTROS`
      .. include:: variables/SANITY_TESTED_DISTROS.rst

   :term:`SBOM_CVE_CHECK_EXPORT_VARS`
      .. include:: variables/SBOM_CVE_CHECK_EXPORT_VARS.rst

   :term:`SBOM_CVE_CHECK_EXTRA_ARGS`
      .. include:: variables/SBOM_CVE_CHECK_EXTRA_ARGS.rst

   :term:`SBOM_CVE_CHECK_SCAN_SCOPE`
      .. include:: variables/SBOM_CVE_CHECK_SCAN_SCOPE.rst

   :term:`SBOM_CVE_CHECK_SHOW_WARNINGS`
      .. include:: variables/SBOM_CVE_CHECK_SHOW_WARNINGS.rst

   :term:`SDK_ARCH`
      .. include:: variables/SDK_ARCH.rst

   :term:`SDK_ARCHIVE_TYPE`
      .. include:: variables/SDK_ARCHIVE_TYPE.rst

   :term:`SDK_AS_ARCH`
      .. include:: variables/SDK_AS_ARCH.rst

   :term:`SDK_BUILDINFO_FILE`
      .. include:: variables/SDK_BUILDINFO_FILE.rst

   :term:`SDK_CC_ARCH`
      .. include:: variables/SDK_CC_ARCH.rst

   :term:`SDK_CUSTOM_TEMPLATECONF`
      .. include:: variables/SDK_CUSTOM_TEMPLATECONF.rst

   :term:`SDK_DEPLOY`
      .. include:: variables/SDK_DEPLOY.rst

   :term:`SDK_DIR`
      .. include:: variables/SDK_DIR.rst

   :term:`SDK_EXT_TYPE`
      .. include:: variables/SDK_EXT_TYPE.rst

   :term:`SDK_HOST_MANIFEST`
      .. include:: variables/SDK_HOST_MANIFEST.rst

   :term:`SDK_INCLUDE_PKGDATA`
      .. include:: variables/SDK_INCLUDE_PKGDATA.rst

   :term:`SDK_INCLUDE_TOOLCHAIN`
      .. include:: variables/SDK_INCLUDE_TOOLCHAIN.rst

   :term:`SDK_LD_ARCH`
      .. include:: variables/SDK_LD_ARCH.rst

   :term:`SDK_NAME`
      .. include:: variables/SDK_NAME.rst

   :term:`SDK_OS`
      .. include:: variables/SDK_OS.rst

   :term:`SDK_OUTPUT`
      .. include:: variables/SDK_OUTPUT.rst

   :term:`SDK_PACKAGE_ARCHS`
      .. include:: variables/SDK_PACKAGE_ARCHS.rst

   :term:`SDK_POSTPROCESS_COMMAND`
      .. include:: variables/SDK_POSTPROCESS_COMMAND.rst

   :term:`SDK_PREFIX`
      .. include:: variables/SDK_PREFIX.rst

   :term:`SDK_RECRDEP_TASKS`
      .. include:: variables/SDK_RECRDEP_TASKS.rst

   :term:`SDK_SYS`
      .. include:: variables/SDK_SYS.rst

   :term:`SDK_TARGET_MANIFEST`
      .. include:: variables/SDK_TARGET_MANIFEST.rst

   :term:`SDK_TARGETS`
      .. include:: variables/SDK_TARGETS.rst

   :term:`SDK_TITLE`
      .. include:: variables/SDK_TITLE.rst

   :term:`SDK_TOOLCHAIN_LANGS`
      .. include:: variables/SDK_TOOLCHAIN_LANGS.rst

   :term:`SDK_UPDATE_URL`
      .. include:: variables/SDK_UPDATE_URL.rst

   :term:`SDK_VENDOR`
      .. include:: variables/SDK_VENDOR.rst

   :term:`SDK_VERSION`
      .. include:: variables/SDK_VERSION.rst

   :term:`SDK_ZIP_OPTIONS`
      .. include:: variables/SDK_ZIP_OPTIONS.rst

   :term:`SDKEXTPATH`
      .. include:: variables/SDKEXTPATH.rst

   :term:`SDKIMAGE_FEATURES`
      .. include:: variables/SDKIMAGE_FEATURES.rst

   :term:`SDKMACHINE`
      .. include:: variables/SDKMACHINE.rst

   :term:`SDKPATH`
      .. include:: variables/SDKPATH.rst

   :term:`SDKPATHINSTALL`
      .. include:: variables/SDKPATHINSTALL.rst

   :term:`SDKTARGETSYSROOT`
      .. include:: variables/SDKTARGETSYSROOT.rst

   :term:`SECTION`
      .. include:: variables/SECTION.rst

   :term:`SELECTED_OPTIMIZATION`
      .. include:: variables/SELECTED_OPTIMIZATION.rst

   :term:`SERIAL_CONSOLES`
      .. include:: variables/SERIAL_CONSOLES.rst

   :term:`SETUPTOOLS_BUILD_ARGS`
      .. include:: variables/SETUPTOOLS_BUILD_ARGS.rst

   :term:`SETUPTOOLS_SETUP_PATH`
      .. include:: variables/SETUPTOOLS_SETUP_PATH.rst

   :term:`SIGGEN_EXCLUDE_SAFE_RECIPE_DEPS`
      .. include:: variables/SIGGEN_EXCLUDE_SAFE_RECIPE_DEPS.rst

   :term:`SIGGEN_EXCLUDERECIPES_ABISAFE`
      .. include:: variables/SIGGEN_EXCLUDERECIPES_ABISAFE.rst

   :term:`SIGGEN_LOCKEDSIGS`
      .. include:: variables/SIGGEN_LOCKEDSIGS.rst

   :term:`SIGGEN_LOCKEDSIGS_TASKSIG_CHECK`
      .. include:: variables/SIGGEN_LOCKEDSIGS_TASKSIG_CHECK.rst

   :term:`SIGGEN_LOCKEDSIGS_TYPES`
      .. include:: variables/SIGGEN_LOCKEDSIGS_TYPES.rst

   :term:`SITEINFO_BITS`
      .. include:: variables/SITEINFO_BITS.rst

   :term:`SITEINFO_ENDIANNESS`
      .. include:: variables/SITEINFO_ENDIANNESS.rst

   :term:`SKIP_FILEDEPS`
      .. include:: variables/SKIP_FILEDEPS.rst

   :term:`SKIP_RECIPE`
      .. include:: variables/SKIP_RECIPE.rst

   :term:`SOC_FAMILY`
      .. include:: variables/SOC_FAMILY.rst

   :term:`SOLIBS`
      .. include:: variables/SOLIBS.rst

   :term:`SOLIBSDEV`
      .. include:: variables/SOLIBSDEV.rst

   :term:`SOURCE_DATE_EPOCH`
      .. include:: variables/SOURCE_DATE_EPOCH.rst

   :term:`SOURCE_MIRROR_FETCH`
      .. include:: variables/SOURCE_MIRROR_FETCH.rst

   :term:`SOURCE_MIRROR_URL`
      .. include:: variables/SOURCE_MIRROR_URL.rst

   :term:`SPDX_BUILD_HOST`
      .. include:: variables/SPDX_BUILD_HOST.rst

   :term:`SPDX_CONCLUDED_LICENSE`
      .. include:: variables/SPDX_CONCLUDED_LICENSE.rst

   :term:`SPDX_CUSTOM_ANNOTATION_VARS`
      .. include:: variables/SPDX_CUSTOM_ANNOTATION_VARS.rst

   :term:`SPDX_FILE_EXCLUDE_PATTERNS`
      .. include:: variables/SPDX_FILE_EXCLUDE_PATTERNS.rst

   :term:`SPDX_GIT_PURL_MAPPINGS`
      .. include:: variables/SPDX_GIT_PURL_MAPPINGS.rst

   :term:`SPDX_IMAGE_SUPPLIER`
      .. include:: variables/SPDX_IMAGE_SUPPLIER.rst

   :term:`SPDX_INCLUDE_BITBAKE_PARENT_BUILD`
      .. include:: variables/SPDX_INCLUDE_BITBAKE_PARENT_BUILD.rst

   :term:`SPDX_INCLUDE_COMPILED_SOURCES`
      .. include:: variables/SPDX_INCLUDE_COMPILED_SOURCES.rst

   :term:`SPDX_INCLUDE_KERNEL_CONFIG`
      .. include:: variables/SPDX_INCLUDE_KERNEL_CONFIG.rst

   :term:`SPDX_INCLUDE_PACKAGECONFIG`
      .. include:: variables/SPDX_INCLUDE_PACKAGECONFIG.rst

   :term:`SPDX_INCLUDE_SOURCES`
      .. include:: variables/SPDX_INCLUDE_SOURCES.rst

   :term:`SPDX_INCLUDE_VEX`
      .. include:: variables/SPDX_INCLUDE_VEX.rst

   :term:`SPDX_INVOKED_BY`
      .. include:: variables/SPDX_INVOKED_BY.rst

   :term:`SPDX_LICENSES`
      .. include:: variables/SPDX_LICENSES.rst

   :term:`SPDX_MULTILIB_SSTATE_ARCHS`
      .. include:: variables/SPDX_MULTILIB_SSTATE_ARCHS.rst

   :term:`SPDX_NAMESPACE_PREFIX`
      .. include:: variables/SPDX_NAMESPACE_PREFIX.rst

   :term:`SPDX_ON_BEHALF_OF`
      .. include:: variables/SPDX_ON_BEHALF_OF.rst

   :term:`SPDX_PACKAGE_SUPPLIER`
      .. include:: variables/SPDX_PACKAGE_SUPPLIER.rst

   :term:`SPDX_PACKAGE_URL`
      .. include:: variables/SPDX_PACKAGE_URL.rst

   :term:`SPDX_PACKAGE_URLS`
      .. include:: variables/SPDX_PACKAGE_URLS.rst

   :term:`SPDX_PACKAGE_VERSION`
      .. include:: variables/SPDX_PACKAGE_VERSION.rst

   :term:`SPDX_PRETTY`
      .. include:: variables/SPDX_PRETTY.rst

   :term:`SPDX_SDK_SUPPLIER`
      .. include:: variables/SPDX_SDK_SUPPLIER.rst

   :term:`SPDX_UUID_NAMESPACE`
      .. include:: variables/SPDX_UUID_NAMESPACE.rst

   :term:`SPDXLICENSEMAP`
      .. include:: variables/SPDXLICENSEMAP.rst

   :term:`SPECIAL_PKGSUFFIX`
      .. include:: variables/SPECIAL_PKGSUFFIX.rst

   :term:`SPL_BINARY`
      .. include:: variables/SPL_BINARY.rst

   :term:`SPL_DTB_BINARY`
      .. include:: variables/SPL_DTB_BINARY.rst

   :term:`SPL_MKIMAGE_DTCOPTS`
      .. include:: variables/SPL_MKIMAGE_DTCOPTS.rst

   :term:`SPL_SIGN_ENABLE`
      .. include:: variables/SPL_SIGN_ENABLE.rst

   :term:`SPL_SIGN_KEYDIR`
      .. include:: variables/SPL_SIGN_KEYDIR.rst

   :term:`SPL_SIGN_KEYNAME`
      .. include:: variables/SPL_SIGN_KEYNAME.rst

   :term:`SPLASH`
      .. include:: variables/SPLASH.rst

   :term:`SPLASH_IMAGES`
      .. include:: variables/SPLASH_IMAGES.rst

   :term:`SRC_URI`
      .. include:: variables/SRC_URI.rst

   :term:`SRC_URI_OVERRIDES_PACKAGE_ARCH`
      .. include:: variables/SRC_URI_OVERRIDES_PACKAGE_ARCH.rst

   :term:`SRCDATE`
      .. include:: variables/SRCDATE.rst

   :term:`SRCPV`
      .. include:: variables/SRCPV.rst

   :term:`SRCREV`
      .. include:: variables/SRCREV.rst

   :term:`SRCREV_FORMAT`
      .. include:: variables/SRCREV_FORMAT.rst

   :term:`SRCTREECOVEREDTASKS`
      .. include:: variables/SRCTREECOVEREDTASKS.rst

   :term:`SSTATE_DIR`
      .. include:: variables/SSTATE_DIR.rst

   :term:`SSTATE_EXCLUDEDEPS_SYSROOT`
      .. include:: variables/SSTATE_EXCLUDEDEPS_SYSROOT.rst

   :term:`SSTATE_MIRROR_ALLOW_NETWORK`
      .. include:: variables/SSTATE_MIRROR_ALLOW_NETWORK.rst

   :term:`SSTATE_MIRRORS`
      .. include:: variables/SSTATE_MIRRORS.rst

   :term:`SSTATE_SCAN_FILES`
      .. include:: variables/SSTATE_SCAN_FILES.rst

   :term:`SSTATE_SIG_KEY`
      .. include:: variables/SSTATE_SIG_KEY.rst

   :term:`SSTATE_SIG_PASSPHRASE`
      .. include:: variables/SSTATE_SIG_PASSPHRASE.rst

   :term:`SSTATE_SKIP_CREATION`
      .. include:: variables/SSTATE_SKIP_CREATION.rst

   :term:`SSTATE_VALID_SIGS`
      .. include:: variables/SSTATE_VALID_SIGS.rst

   :term:`SSTATE_VERIFY_SIG`
      .. include:: variables/SSTATE_VERIFY_SIG.rst

   :term:`STABLE_VERSION_PARTS`
      .. include:: variables/STABLE_VERSION_PARTS.rst

   :term:`STAGING_BASE_LIBDIR_NATIVE`
      .. include:: variables/STAGING_BASE_LIBDIR_NATIVE.rst

   :term:`STAGING_BASELIBDIR`
      .. include:: variables/STAGING_BASELIBDIR.rst

   :term:`STAGING_BINDIR`
      .. include:: variables/STAGING_BINDIR.rst

   :term:`STAGING_BINDIR_CROSS`
      .. include:: variables/STAGING_BINDIR_CROSS.rst

   :term:`STAGING_BINDIR_NATIVE`
      .. include:: variables/STAGING_BINDIR_NATIVE.rst

   :term:`STAGING_DATADIR`
      .. include:: variables/STAGING_DATADIR.rst

   :term:`STAGING_DATADIR_NATIVE`
      .. include:: variables/STAGING_DATADIR_NATIVE.rst

   :term:`STAGING_DIR`
      .. include:: variables/STAGING_DIR.rst

   :term:`STAGING_DIR_HOST`
      .. include:: variables/STAGING_DIR_HOST.rst

   :term:`STAGING_DIR_NATIVE`
      .. include:: variables/STAGING_DIR_NATIVE.rst

   :term:`STAGING_DIR_TARGET`
      .. include:: variables/STAGING_DIR_TARGET.rst

   :term:`STAGING_ETCDIR_NATIVE`
      .. include:: variables/STAGING_ETCDIR_NATIVE.rst

   :term:`STAGING_EXECPREFIXDIR`
      .. include:: variables/STAGING_EXECPREFIXDIR.rst

   :term:`STAGING_INCDIR`
      .. include:: variables/STAGING_INCDIR.rst

   :term:`STAGING_INCDIR_NATIVE`
      .. include:: variables/STAGING_INCDIR_NATIVE.rst

   :term:`STAGING_KERNEL_BUILDDIR`
      .. include:: variables/STAGING_KERNEL_BUILDDIR.rst

   :term:`STAGING_KERNEL_DIR`
      .. include:: variables/STAGING_KERNEL_DIR.rst

   :term:`STAGING_LIBDIR`
      .. include:: variables/STAGING_LIBDIR.rst

   :term:`STAGING_LIBDIR_NATIVE`
      .. include:: variables/STAGING_LIBDIR_NATIVE.rst

   :term:`STAMP`
      .. include:: variables/STAMP.rst

   :term:`STAMPCLEAN`
      .. include:: variables/STAMPCLEAN.rst

   :term:`STAMPS_DIR`
      .. include:: variables/STAMPS_DIR.rst

   :term:`STRIP`
      .. include:: variables/STRIP.rst

   :term:`SUMMARY`
      .. include:: variables/SUMMARY.rst

   :term:`SVNDIR`
      .. include:: variables/SVNDIR.rst

   :term:`SYSLINUX_DEFAULT_CONSOLE`
      .. include:: variables/SYSLINUX_DEFAULT_CONSOLE.rst

   :term:`SYSLINUX_OPTS`
      .. include:: variables/SYSLINUX_OPTS.rst

   :term:`SYSLINUX_SERIAL`
      .. include:: variables/SYSLINUX_SERIAL.rst

   :term:`SYSLINUX_SERIAL_TTY`
      .. include:: variables/SYSLINUX_SERIAL_TTY.rst

   :term:`SYSLINUX_SPLASH`
      .. include:: variables/SYSLINUX_SPLASH.rst

   :term:`SYSROOT_DESTDIR`
      .. include:: variables/SYSROOT_DESTDIR.rst

   :term:`SYSROOT_DIRS`
      .. include:: variables/SYSROOT_DIRS.rst

   :term:`SYSROOT_DIRS_IGNORE`
      .. include:: variables/SYSROOT_DIRS_IGNORE.rst

   :term:`SYSROOT_DIRS_NATIVE`
      .. include:: variables/SYSROOT_DIRS_NATIVE.rst

   :term:`SYSROOT_PREPROCESS_FUNCS`
      .. include:: variables/SYSROOT_PREPROCESS_FUNCS.rst

   :term:`SYSTEMD_AUTO_ENABLE`
      .. include:: variables/SYSTEMD_AUTO_ENABLE.rst

   :term:`SYSTEMD_BOOT_CFG`
      .. include:: variables/SYSTEMD_BOOT_CFG.rst

   :term:`SYSTEMD_BOOT_ENTRIES`
      .. include:: variables/SYSTEMD_BOOT_ENTRIES.rst

   :term:`SYSTEMD_BOOT_TIMEOUT`
      .. include:: variables/SYSTEMD_BOOT_TIMEOUT.rst

   :term:`SYSTEMD_DEFAULT_TARGET`
      .. include:: variables/SYSTEMD_DEFAULT_TARGET.rst

   :term:`SYSTEMD_PACKAGES`
      .. include:: variables/SYSTEMD_PACKAGES.rst

   :term:`SYSTEMD_SERVICE`
      .. include:: variables/SYSTEMD_SERVICE.rst

   :term:`SYSVINIT_ENABLED_GETTYS`
      .. include:: variables/SYSVINIT_ENABLED_GETTYS.rst

   :term:`T`
      .. include:: variables/T.rst

   :term:`TARGET_ARCH`
      .. include:: variables/TARGET_ARCH.rst

   :term:`TARGET_AS_ARCH`
      .. include:: variables/TARGET_AS_ARCH.rst

   :term:`TARGET_CC_ARCH`
      .. include:: variables/TARGET_CC_ARCH.rst

   :term:`TARGET_CC_KERNEL_ARCH`
      .. include:: variables/TARGET_CC_KERNEL_ARCH.rst

   :term:`TARGET_CFLAGS`
      .. include:: variables/TARGET_CFLAGS.rst

   :term:`TARGET_CPPFLAGS`
      .. include:: variables/TARGET_CPPFLAGS.rst

   :term:`TARGET_CXXFLAGS`
      .. include:: variables/TARGET_CXXFLAGS.rst

   :term:`TARGET_DBGSRC_DIR`
      .. include:: variables/TARGET_DBGSRC_DIR.rst

   :term:`TARGET_FPU`
      .. include:: variables/TARGET_FPU.rst

   :term:`TARGET_LD_ARCH`
      .. include:: variables/TARGET_LD_ARCH.rst

   :term:`TARGET_LDFLAGS`
      .. include:: variables/TARGET_LDFLAGS.rst

   :term:`TARGET_OS`
      .. include:: variables/TARGET_OS.rst

   :term:`TARGET_PREFIX`
      .. include:: variables/TARGET_PREFIX.rst

   :term:`TARGET_SYS`
      .. include:: variables/TARGET_SYS.rst

   :term:`TARGET_VENDOR`
      .. include:: variables/TARGET_VENDOR.rst

   :term:`TC_CXX_RUNTIME`
      .. include:: variables/TC_CXX_RUNTIME.rst

   :term:`TCLIBC`
      .. include:: variables/TCLIBC.rst

   :term:`TCMODE`
      .. include:: variables/TCMODE.rst

   :term:`TEMPLATECONF`
      .. include:: variables/TEMPLATECONF.rst

   :term:`TEST_EXPORT_DIR`
      .. include:: variables/TEST_EXPORT_DIR.rst

   :term:`TEST_EXPORT_ONLY`
      .. include:: variables/TEST_EXPORT_ONLY.rst

   :term:`TEST_LOG_DIR`
      .. include:: variables/TEST_LOG_DIR.rst

   :term:`TEST_POWERCONTROL_CMD`
      .. include:: variables/TEST_POWERCONTROL_CMD.rst

   :term:`TEST_POWERCONTROL_EXTRA_ARGS`
      .. include:: variables/TEST_POWERCONTROL_EXTRA_ARGS.rst

   :term:`TEST_QEMUBOOT_TIMEOUT`
      .. include:: variables/TEST_QEMUBOOT_TIMEOUT.rst

   :term:`TEST_SERIALCONTROL_CMD`
      .. include:: variables/TEST_SERIALCONTROL_CMD.rst

   :term:`TEST_SERIALCONTROL_CONNECT_TIMEOUT`
      .. include:: variables/TEST_SERIALCONTROL_CONNECT_TIMEOUT.rst

   :term:`TEST_SERIALCONTROL_EXTRA_ARGS`
      .. include:: variables/TEST_SERIALCONTROL_EXTRA_ARGS.rst

   :term:`TEST_SERIALCONTROL_PS1`
      .. include:: variables/TEST_SERIALCONTROL_PS1.rst

   :term:`TEST_SERVER_IP`
      .. include:: variables/TEST_SERVER_IP.rst

   :term:`TEST_SUITES`
      .. include:: variables/TEST_SUITES.rst

   :term:`TEST_TARGET`
      .. include:: variables/TEST_TARGET.rst

   :term:`TEST_TARGET_IP`
      .. include:: variables/TEST_TARGET_IP.rst

   :term:`TESTIMAGE_AUTO`
      .. include:: variables/TESTIMAGE_AUTO.rst

   :term:`TESTIMAGE_FAILED_QA_ARTIFACTS`
      .. include:: variables/TESTIMAGE_FAILED_QA_ARTIFACTS.rst

   :term:`TESTSDK_SUITES`
      .. include:: variables/TESTSDK_SUITES.rst

   :term:`THISDIR`
      .. include:: variables/THISDIR.rst

   :term:`TIME`
      .. include:: variables/TIME.rst

   :term:`TMPDIR`
      .. include:: variables/TMPDIR.rst

   :term:`TOOLCHAIN`
      .. include:: variables/TOOLCHAIN.rst

   :term:`TOOLCHAIN_HOST_TASK`
      .. include:: variables/TOOLCHAIN_HOST_TASK.rst

   :term:`TOOLCHAIN_HOST_TASK_ESDK`
      .. include:: variables/TOOLCHAIN_HOST_TASK_ESDK.rst

   :term:`TOOLCHAIN_NATIVE`
      .. include:: variables/TOOLCHAIN_NATIVE.rst

   :term:`TOOLCHAIN_OPTIONS`
      .. include:: variables/TOOLCHAIN_OPTIONS.rst

   :term:`TOOLCHAIN_OUTPUTNAME`
      .. include:: variables/TOOLCHAIN_OUTPUTNAME.rst

   :term:`TOOLCHAIN_TARGET_TASK`
      .. include:: variables/TOOLCHAIN_TARGET_TASK.rst

   :term:`TOPDIR`
      .. include:: variables/TOPDIR.rst

   :term:`TRANSLATED_TARGET_ARCH`
      .. include:: variables/TRANSLATED_TARGET_ARCH.rst

   :term:`TUNE_ARCH`
      .. include:: variables/TUNE_ARCH.rst

   :term:`TUNE_ASARGS`
      .. include:: variables/TUNE_ASARGS.rst

   :term:`TUNE_CCARGS`
      .. include:: variables/TUNE_CCARGS.rst

   :term:`TUNE_FEATURES`
      .. include:: variables/TUNE_FEATURES.rst

   :term:`TUNE_LDARGS`
      .. include:: variables/TUNE_LDARGS.rst

   :term:`TUNE_PKGARCH`
      .. include:: variables/TUNE_PKGARCH.rst

   :term:`TUNECONFLICTS[feature]`
      .. include:: variables/TUNECONFLICTS[feature].rst

   :term:`TUNEVALID[feature]`
      .. include:: variables/TUNEVALID[feature].rst

   :term:`UBOOT_BINARY`
      .. include:: variables/UBOOT_BINARY.rst

   :term:`UBOOT_CONFIG`
      .. include:: variables/UBOOT_CONFIG.rst

   :term:`UBOOT_CONFIG_BINARY`
      .. include:: variables/UBOOT_CONFIG_BINARY.rst

   :term:`UBOOT_CONFIG_FRAGMENTS`
      .. include:: variables/UBOOT_CONFIG_FRAGMENTS.rst

   :term:`UBOOT_CONFIG_IMAGE_FSTYPES`
      .. include:: variables/UBOOT_CONFIG_IMAGE_FSTYPES.rst

   :term:`UBOOT_CONFIG_MAKE_OPTS`
      .. include:: variables/UBOOT_CONFIG_MAKE_OPTS.rst

   :term:`UBOOT_DTB_LOADADDRESS`
      .. include:: variables/UBOOT_DTB_LOADADDRESS.rst

   :term:`UBOOT_DTBO_LOADADDRESS`
      .. include:: variables/UBOOT_DTBO_LOADADDRESS.rst

   :term:`UBOOT_ENTRYPOINT`
      .. include:: variables/UBOOT_ENTRYPOINT.rst

   :term:`UBOOT_ENV`
      .. include:: variables/UBOOT_ENV.rst

   :term:`UBOOT_ENV_SRC_SUFFIX`
      .. include:: variables/UBOOT_ENV_SRC_SUFFIX.rst

   :term:`UBOOT_ENV_SUFFIX`
      .. include:: variables/UBOOT_ENV_SUFFIX.rst

   :term:`UBOOT_FIT_ADDRESS_CELLS`
      .. include:: variables/UBOOT_FIT_ADDRESS_CELLS.rst

   :term:`UBOOT_FIT_ARM_TRUSTED_FIRMWARE`
      .. include:: variables/UBOOT_FIT_ARM_TRUSTED_FIRMWARE.rst

   :term:`UBOOT_FIT_ARM_TRUSTED_FIRMWARE_IMAGE`
      .. include:: variables/UBOOT_FIT_ARM_TRUSTED_FIRMWARE_IMAGE.rst

   :term:`UBOOT_FIT_CONF_DESC`
      .. include:: variables/UBOOT_FIT_CONF_DESC.rst

   :term:`UBOOT_FIT_CONF_FIRMWARE`
      .. include:: variables/UBOOT_FIT_CONF_FIRMWARE.rst

   :term:`UBOOT_FIT_CONF_USER_LOADABLES`
      .. include:: variables/UBOOT_FIT_CONF_USER_LOADABLES.rst

   :term:`UBOOT_FIT_DESC`
      .. include:: variables/UBOOT_FIT_DESC.rst

   :term:`UBOOT_FIT_GENERATE_KEYS`
      .. include:: variables/UBOOT_FIT_GENERATE_KEYS.rst

   :term:`UBOOT_FIT_HASH_ALG`
      .. include:: variables/UBOOT_FIT_HASH_ALG.rst

   :term:`UBOOT_FIT_KEY_GENRSA_ARGS`
      .. include:: variables/UBOOT_FIT_KEY_GENRSA_ARGS.rst

   :term:`UBOOT_FIT_KEY_REQ_ARGS`
      .. include:: variables/UBOOT_FIT_KEY_REQ_ARGS.rst

   :term:`UBOOT_FIT_KEY_SIGN_PKCS`
      .. include:: variables/UBOOT_FIT_KEY_SIGN_PKCS.rst

   :term:`UBOOT_FIT_SIGN_ALG`
      .. include:: variables/UBOOT_FIT_SIGN_ALG.rst

   :term:`UBOOT_FIT_SIGN_NUMBITS`
      .. include:: variables/UBOOT_FIT_SIGN_NUMBITS.rst

   :term:`UBOOT_FIT_TEE`
      .. include:: variables/UBOOT_FIT_TEE.rst

   :term:`UBOOT_FIT_TEE_IMAGE`
      .. include:: variables/UBOOT_FIT_TEE_IMAGE.rst

   :term:`UBOOT_FIT_USER_SETTINGS`
      .. include:: variables/UBOOT_FIT_USER_SETTINGS.rst

   :term:`UBOOT_FITIMAGE_ENABLE`
      .. include:: variables/UBOOT_FITIMAGE_ENABLE.rst

   :term:`UBOOT_FRAGMENTS`
      .. include:: variables/UBOOT_FRAGMENTS.rst

   :term:`UBOOT_INITIAL_ENV_BINARY`
      .. include:: variables/UBOOT_INITIAL_ENV_BINARY.rst

   :term:`UBOOT_INITIAL_ENV_BINARY_REDUND`
      .. include:: variables/UBOOT_INITIAL_ENV_BINARY_REDUND.rst

   :term:`UBOOT_INITIAL_ENV_BINARY_SIZE`
      .. include:: variables/UBOOT_INITIAL_ENV_BINARY_SIZE.rst

   :term:`UBOOT_LOADADDRESS`
      .. include:: variables/UBOOT_LOADADDRESS.rst

   :term:`UBOOT_LOCALVERSION`
      .. include:: variables/UBOOT_LOCALVERSION.rst

   :term:`UBOOT_MACHINE`
      .. include:: variables/UBOOT_MACHINE.rst

   :term:`UBOOT_MAKE_OPTS`
      .. include:: variables/UBOOT_MAKE_OPTS.rst

   :term:`UBOOT_MAKE_TARGET`
      .. include:: variables/UBOOT_MAKE_TARGET.rst

   :term:`UBOOT_MKIMAGE`
      .. include:: variables/UBOOT_MKIMAGE.rst

   :term:`UBOOT_MKIMAGE_DTCOPTS`
      .. include:: variables/UBOOT_MKIMAGE_DTCOPTS.rst

   :term:`UBOOT_MKIMAGE_KERNEL_TYPE`
      .. include:: variables/UBOOT_MKIMAGE_KERNEL_TYPE.rst

   :term:`UBOOT_MKIMAGE_SIGN`
      .. include:: variables/UBOOT_MKIMAGE_SIGN.rst

   :term:`UBOOT_MKIMAGE_SIGN_ARGS`
      .. include:: variables/UBOOT_MKIMAGE_SIGN_ARGS.rst

   :term:`UBOOT_RD_ENTRYPOINT`
      .. include:: variables/UBOOT_RD_ENTRYPOINT.rst

   :term:`UBOOT_RD_LOADADDRESS`
      .. include:: variables/UBOOT_RD_LOADADDRESS.rst

   :term:`UBOOT_SIGN_ENABLE`
      .. include:: variables/UBOOT_SIGN_ENABLE.rst

   :term:`UBOOT_SIGN_KEYDIR`
      .. include:: variables/UBOOT_SIGN_KEYDIR.rst

   :term:`UBOOT_SIGN_KEYNAME`
      .. include:: variables/UBOOT_SIGN_KEYNAME.rst

   :term:`UBOOT_SUFFIX`
      .. include:: variables/UBOOT_SUFFIX.rst

   :term:`UBOOT_TARGET`
      .. include:: variables/UBOOT_TARGET.rst

   :term:`UBOOT_VERSION`
      .. include:: variables/UBOOT_VERSION.rst

   :term:`UKI_CMDLINE`
      .. include:: variables/UKI_CMDLINE.rst

   :term:`UKI_CONFIG_FILE`
      .. include:: variables/UKI_CONFIG_FILE.rst

   :term:`UKI_DEVICETREE`
      .. include:: variables/UKI_DEVICETREE.rst

   :term:`UKI_FILENAME`
      .. include:: variables/UKI_FILENAME.rst

   :term:`UKI_KERNEL_FILENAME`
      .. include:: variables/UKI_KERNEL_FILENAME.rst

   :term:`UKI_SB_CERT`
      .. include:: variables/UKI_SB_CERT.rst

   :term:`UKI_SB_KEY`
      .. include:: variables/UKI_SB_KEY.rst

   :term:`UKIFY_CMD`
      .. include:: variables/UKIFY_CMD.rst

   :term:`UNINATIVE_CHECKSUM`
      .. include:: variables/UNINATIVE_CHECKSUM.rst

   :term:`UNINATIVE_URL`
      .. include:: variables/UNINATIVE_URL.rst

   :term:`UNKNOWN_CONFIGURE_OPT_IGNORE`
      .. include:: variables/UNKNOWN_CONFIGURE_OPT_IGNORE.rst

   :term:`UNPACKDIR`
      .. include:: variables/UNPACKDIR.rst

   :term:`UPDATERCPN`
      .. include:: variables/UPDATERCPN.rst

   :term:`UPSTREAM_CHECK_COMMITS`
      .. include:: variables/UPSTREAM_CHECK_COMMITS.rst

   :term:`UPSTREAM_CHECK_GITTAGREGEX`
      .. include:: variables/UPSTREAM_CHECK_GITTAGREGEX.rst

   :term:`UPSTREAM_CHECK_REGEX`
      .. include:: variables/UPSTREAM_CHECK_REGEX.rst

   :term:`UPSTREAM_CHECK_URI`
      .. include:: variables/UPSTREAM_CHECK_URI.rst

   :term:`UPSTREAM_STABLE_RELEASE_REGEX`
      .. include:: variables/UPSTREAM_STABLE_RELEASE_REGEX.rst

   :term:`UPSTREAM_VERSION_UNKNOWN`
      .. include:: variables/UPSTREAM_VERSION_UNKNOWN.rst

   :term:`USE_DEVFS`
      .. include:: variables/USE_DEVFS.rst

   :term:`USE_NLS`
      .. include:: variables/USE_NLS.rst

   :term:`USE_VT`
      .. include:: variables/USE_VT.rst

   :term:`USER_CLASSES`
      .. include:: variables/USER_CLASSES.rst

   :term:`USERADD_DEPENDS`
      .. include:: variables/USERADD_DEPENDS.rst

   :term:`USERADD_ERROR_DYNAMIC`
      .. include:: variables/USERADD_ERROR_DYNAMIC.rst

   :term:`USERADD_GID_TABLES`
      .. include:: variables/USERADD_GID_TABLES.rst

   :term:`USERADD_PACKAGES`
      .. include:: variables/USERADD_PACKAGES.rst

   :term:`USERADD_PARAM`
      .. include:: variables/USERADD_PARAM.rst

   :term:`USERADD_UID_TABLES`
      .. include:: variables/USERADD_UID_TABLES.rst

   :term:`USERADDEXTENSION`
      .. include:: variables/USERADDEXTENSION.rst

   :term:`USERMOD_PARAMS`
      .. include:: variables/USERMOD_PARAMS.rst

   :term:`VIRTUAL-RUNTIME`
      .. include:: variables/VIRTUAL-RUNTIME.rst

   :term:`WARN_QA`
      .. include:: variables/WARN_QA.rst

   :term:`WATCHDOG_RUNTIME_SEC`
      .. include:: variables/WATCHDOG_RUNTIME_SEC.rst

   :term:`WATCHDOG_TIMEOUT`
      .. include:: variables/WATCHDOG_TIMEOUT.rst

   :term:`WESTON_USER`
      .. include:: variables/WESTON_USER.rst

   :term:`WESTON_USER_HOME`
      .. include:: variables/WESTON_USER_HOME.rst

   :term:`WIC_CREATE_EXTRA_ARGS`
      .. include:: variables/WIC_CREATE_EXTRA_ARGS.rst

   :term:`WIC_SECTOR_SIZE`
      .. include:: variables/WIC_SECTOR_SIZE.rst

   :term:`WIRELESS_DAEMON`
      .. include:: variables/WIRELESS_DAEMON.rst

   :term:`WKS_FILE`
      .. include:: variables/WKS_FILE.rst

   :term:`WKS_FILE_DEPENDS`
      .. include:: variables/WKS_FILE_DEPENDS.rst

   :term:`WKS_FILES`
      .. include:: variables/WKS_FILES.rst

   :term:`WORKDIR`
      .. include:: variables/WORKDIR.rst

   :term:`XSERVER`
      .. include:: variables/XSERVER.rst

   :term:`XZ_MEMLIMIT`
      .. include:: variables/XZ_MEMLIMIT.rst

   :term:`XZ_THREADS`
      .. include:: variables/XZ_THREADS.rst

   :term:`ZSTD_COMPRESSION_LEVEL`
      .. include:: variables/ZSTD_COMPRESSION_LEVEL.rst

   :term:`ZSTD_THREADS`
      .. include:: variables/ZSTD_THREADS.rst


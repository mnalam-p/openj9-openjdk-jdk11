# ===========================================================================
# Portions Copyright 2018, 2018 IBM Corporation.
# ===========================================================================
# This code is free software; you can redistribute it and/or modify it
# under the terms of the GNU General Public License version 2 only, as
# published by the Free Software Foundation.
#
# IBM designates this particular file as subject to the "Classpath" exception 
# as provided by IBM in the LICENSE file that accompanied this code.
#
# This code is distributed in the hope that it will be useful, but WITHOUT
# ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or
# FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License
# version 2 for more details (a copy is included in the LICENSE file that
# accompanied this code).
#
# You should have received a copy of the GNU General Public License version
# 2 along with this work; if not, see <http://www.gnu.org/licenses/>.
# ===========================================================================

# This file identifies the root of the test-suite hierarchy.
# It also contains test-suite configuration information.

# The list of keywords supported in the entire test suite.  The
# "intermittent" keyword marks tests known to fail intermittently.
# The "randomness" keyword marks tests using randomness with test
# cases differing from run to run. (A test using a fixed random seed
# would not count as "randomness" by this definition.) Extra care
# should be taken to handle test failures of intermittent or
# randomness tests.
#
# A "headful" test requires a graphical environment to meaningfully
# run. Tests that are not headful are "headless".
# A test flagged with key "printer" requires a printer to succeed, else
# throws a PrinterException or the like.

keys=2d dnd headful i18n intermittent printer randomness jfr

# Tests that must run in othervm mode
othervm.dirs=java/awt java/beans javax/accessibility javax/imageio javax/sound javax/swing javax/print \
com/apple/laf com/sun/java/accessibility com/sun/java/swing sanity/client demo/jfc \
javax/management com/sun/awt sun/awt sun/java2d javax/xml/jaxp/testng/validation java/lang/ProcessHandle

# Tests that cannot run concurrently
exclusiveAccess.dirs=java/rmi/Naming java/util/prefs sun/management/jmxremote sun/tools/jstatd \
sun/security/mscapi java/util/stream java/util/Arrays/largeMemory java/util/BitSet/stream javax/rmi \
sanity/client

# Group definitions
groups=TEST.groups

# Allow querying of various System properties in @requires clauses
#
# Source files for classes that will be used at the beginning of each test suite run,
# to determine additional characteristics of the system for use with the @requires tag.
# Note: compiled bootlibs code will be located in the folder 'bootClasses'
requires.extraPropDefns = ../../test/jtreg-ext/requires/VMProps.java [../../closed/test/jtreg-ext/requires/VMPropsExt.java]
requires.extraPropDefns.bootlibs = ../../test/lib/sun \
    ../../test/lib/jdk/test/lib/Platform.java \
    ../../test/lib/jdk/test/lib/Container.java
requires.extraPropDefns.vmOpts = -XX:+UnlockDiagnosticVMOptions -XX:+WhiteBoxAPI -Xbootclasspath/a:bootClasses
requires.properties= \
    sun.arch.data.model \
    java.runtime.name \
    vm.gc.Z \
    vm.gc.Shenandoah \
    vm.graal.enabled \
    vm.compiler1.enabled \
    vm.compiler2.enabled \
    vm.cds \
    vm.debug \
    vm.hasSA \
    vm.hasSAandCanAttach \
    vm.hasJFR \
    docker.support \
    release.implementor

# Unset Hotspot VMProps ProdDefns requires class and replace with optional OpenJ9 class
requires.extraPropDefns = [../../closed/test/jtreg-ext/requires/OpenJ9PropsExt.java]

# Minimum jtreg version
requiredVersion=5.1 b1

# Path to libraries in the topmost test directory. This is needed so @library
# does not need ../../ notation to reach them
external.lib.roots = ../../

# Use new module options
useNewOptions=true

# Use --patch-module instead of -Xmodule:
useNewPatchModule=true


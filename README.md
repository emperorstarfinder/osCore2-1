# osCore2 Fork by Bill Blight of Opensim.life

### USE AT YOUR OWN RISK!!

Minimal support is offered for this project at this time, it is a labor of love, and should be not used for production environments unless you are really sure what you are doing.

### USE AT YOUR OWN RISK!!


# Contains the Yengine(formerly XMR) script engine, Xengine still default

XMR script engine Donated to Opensimulator core by, mrieker (DreamNation) and Cores own Melanie.

Notes on Yengine: Although it works very well, it is not compatible with Xengine, meaing crossing or TP'ing into an Yengine region from a Xengine region will result in scripts being reset and may need recompiled.

## BULLETSIM IS REMOVED FROM THIS FORK!!!

## Jopensim support included

I have included the source which will build the Jopensim Profile and Search moduals.
There is no documetation on configuring them included at this point
please see http://jopensim.com for details.

### You will need to remove these modules if you don't plan on using them, as it will cause errors.

This has some fixes that have not made it into core OpenSimulator .

Some of the additions include the http tests branch which improves the built in http server.
Roll back of some of the permission changes , specifcally the item creation permsions for textures.
configureable LSL delays, see OpenSimDefaults.ini, added osParcelMusicURL, for gods, as the ll funcion only works for parcel/land owners.

This build also includes the phpmutelist found at https://github.com/kcozens/OpenSimMutelist

And various others.

Welcome to OpenSim!

# Overview

OpenSim is a BSD Licensed Open Source project to develop a functioning
virtual worlds server platform capable of supporting multiple clients
and servers in a heterogeneous grid structure. OpenSim is written in
C#, and can run under Mono or the Microsoft .NET runtimes.

This is considered an alpha release.  Some stuff works, a lot doesn't.
If it breaks, you get to keep *both* pieces.

## Compiling OpenSim

Please see BUILDING.md if you downloaded a source distribution and
need to build OpenSim before running it.

## Running OpenSim on Windows

You will need .NET 4.6 installed to run this version OpenSimulator.

We recommend that you run OpenSim from a command prompt on Windows in order
to capture any errors.

To run OpenSim from a command prompt

 * cd to the bin/ directory where you unpacked OpenSim
 * run OpenSim.exe

Now see the "Configuring OpenSim" section

## Running OpenSim on Linux


You will need Mono >= 5.x to run this version of OpenSimulator.  On some Linux distributions you
may need to install additional packages.  See http://opensimulator.org/wiki/Dependencies
for more information.

To run OpenSim, from the unpacked distribution type:

 * cd bin
 * mono OpenSim.exe

Now see the "Configuring OpenSim" section
### I'd suggest the following settings in your linux startup script for OpenSim.exe
> ulimit -s 1048576

> export MONO_GC_PARAMS="nursery-size=32m,promotion-age=14,minor=split,major=marksweep,no-lazy-sweep,alloc-ratio=50"

> export MONO_GC_DEBUG=""

> export MONO_ENV_OPTIONS="--desktop"


## Configuring OpenSim

When OpenSim starts for the first time, you will be prompted with a
series of questions that look something like:

        [09-17 03:54:40] DEFAULT REGION CONFIG: Simulator Name [OpenSim Test]:

For all the options except simulator name, you can safely hit enter to accept
the default if you want to connect using a client on the same machine or over
your local network.

You will then be asked "Do you wish to join an existing estate?".  If you're
starting OpenSim for the first time then answer no (which is the default) and
provide an estate name.

Shortly afterwards, you will then be asked to enter an estate owner first name,
last name, password and e-mail (which can be left blank).  Do not forget these
details, since initially only this account will be able to manage your region
in-world.  You can also use these details to perform your first login.

Once you are presented with a prompt that looks like:

        Region (My region name) #

You have successfully started OpenSim.

If you want to create another user account to login rather than the estate
account, then type "create user" on the OpenSim console and follow the prompts.

Helpful resources:
 * http://opensimulator.org/wiki/Configuration
 * http://opensimulator.org/wiki/Configuring_Regions

## Connecting to your OpenSim

By default your sim will be available for login on port 9000.  You can login by
adding -loginuri http://127.0.0.1:9000 to the command that starts Second Life
(e.g. in the Target: box of the client icon properties on Windows).  You can
also login using the network IP address of the machine running OpenSim (e.g.
http://192.168.1.2:9000)

To login, use the avatar details that you gave for your estate ownership or the
one you set up using the "create user" command.

### Bug reports

email grid@opensim.life

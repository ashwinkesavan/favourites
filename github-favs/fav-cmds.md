`git config --global user.name "Ashwin Iyengar"`
`git config --global user.email "****@gmail.com"`
`sudo ufw enable`
`sudo ufw status numbered`
`sudo ufw delete 2`
%% to fix snap-store update pending notfication in app center ubuntu 24.04 lts
Sunday 16 February 2025 08:18:07 AM JST %%
`sudo snap refresh snap-store`

%%22 February 2025 11:00:52 AM JST on pop_os as it does not use grub but systemd-boot and hence below commnds%%
`sudo kernelstub --delete-options "quiet systemd.show_status=false splash"
`sudo kernelstub --add-options "systemd.show_status=true"
`sudo kernelstub --print-config
%% *Saturday 22 Feb 2025 08:37:44 PM JST* %%
`alias date='date +"%A %d %b %Y %T %Z"'
%%22 Feb 2025 08:42:27 PM JST%%
eval $(ssh-agent)
ssh-add

----

%%dnsutils like dig cmd and host cmd does not exists in msys or cygwin because upstream stopped support for windows. Learn to become comfortable with nslookup tool for windows.%%

*Saturday 01 March 2025 06:49:40 AM JST*
%%to customize date and time display format in pop os gnome 46. i installed the following extenstion
'panel date format' in https://extensions.gnome.org/extension/3465/panel-date-format/ and use the locale setting of '%c
Then you can choose to set the below from bash shell cmd prompt to update the seconds display%%
`gsettings set org.gnome.desktop.interface show-clock-seconds true
*Saturday 01 March 2025 01:03:46 PM JST 
%%show week number in panel calendar%%
`gsettings set org.gnome.desktop.calendar show-weekdate true
%%if you want the gnome panel calendar to start the week in monday instead of the locale en_IN.UTF8 default of sunday, then do the following.
in file%% `/usr/share/i18n/locales/en_IN
in the section 
`LC_TIME
add the below two lines first_weekday and first_workday after week 7.. line
`week 7;19971130;1
`first_weekday 2
`first_workday 2
END LC_TIME

---

%%pacman query for list of installed files from a package%%
`pacman -Ql package-name

 *01 Mar 2025 01:51:07 PM JST*
---

*09 Mar 2025 12:38:39 AM JST*
%%to change console font size in Linux
for ubuntu based systems%%
`sudo dpkg-reconfigure console-setup
%%for redhat based systems%%
`sudo dnf reconfigure system-console-setup

*Sunday 09 March 2025 07:48:09 AM JST*
%%Essential shortcut keys in pop (maybe ubuntu also)%% 
`super key + Y` = toggle titling and floating windowing scheme.
super key = launches 'The super cool launcher' in pop. No need to mouse slow clicking. Time to embrace keyboard and ditch mouse.

---

*Sunday 23 March 2025 04:40:49 PM JST*
%%oh-my-posh cmd is awesomely cool. Information on it is available at https://ohmyposh.dev/
package name to install ohmyposh on msys2 is%%
`pacman -S mingw-w64-x86_64-oh-my-posh
%%package nerd font required by ohmyposh%%
`pacman -S mingw-w64-x86_64-nerd-fonts
%%mesloLGM Nerd font is required by posh to display properly%%

----

search for a installed package  *Sunday 30 Mar 2025 02:17:06 PM JST*
`pacman -Q | grep -i packageName

%%dpkg for above (*Sunday 30 March 2025 03:26:31 PM JST*), List all installed pakage without the formatting. In one pkg name per line and you can specify the formatting options optionally.%%
`dpkg-query -W | grep -i pkgName
%%dpkg for owner package of a installed file.%%
`dpkg-query -S /home/ashwin/.local/bin/oh-my-posh`

-------

%%there is no easy way for vim to insert shell output without the new line insertion in :r!cmd format. Have to live with this pain%% *(Sunday 30 March 2025 03:27 JST)*

-----
Saturday 14 June 2025 12:17:42 PM JST
To see warning and error messages since last boot
`journalctl --boot -1 -p warning`
-----

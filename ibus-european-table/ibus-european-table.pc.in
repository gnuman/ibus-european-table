Name:       ibus-european-table
Version:    1.1.0
Release:    1%{?dist}
Summary:    The Table engine for IBus platform
License:    LGPLv2+
Group:      System Environment/Libraries
URL:        http://git.fedorahosted.org/git/?p=ibus-european-table.git
Source0:    https://fedoraproject.org/wiki/File:{name}-%{version}.tar.gz

Requires:       ibus
BuildRequires:  ibus-devel
BuildArch:  noarch

%description
The European Table engine for IBus platform.

%prep
%setup -q

%build
%configure --disable-static --disable-additional
make %{?_smp_mflags}

%install
make DESTDIR=${RPM_BUILD_ROOT} NO_INDEX=true install pkgconfigdir=%{_datadir}/pkgconfig

%find_lang %{name}

%files -f %{name}.lang
%defattr(-,root,root,-)
%doc AUTHORS COPYING README 
%{_datadir}/%{name}
%{_datadir}/ibus/component/european-table.xml
%{_bindir}/%{name}-createdb
%{_libexecdir}/ibus-engine-european-table
%{_datadir}/pkgconfig/%{name}.pc

%changelog
* Tue Dec 5 2011 Anish Patil <anish.developer@gmail.com> - 1.1.0-1
- The first version.
- derieved from ibus-table developed by Yu Yuwei <acevery@gmail.com>

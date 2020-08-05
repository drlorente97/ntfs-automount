# GNU make is required to run this file. To install on *BSD, run:
#   gmake PREFIX=/usr/local install

all:

install:
	install -Dm644 "ntfs-automount.rules" "${DESTDIR}/usr/lib/udev/rules.d/99-ntfs-automount.rules"
	install -Dm647 "ntfs-automount" "${DESTDIR}/usr/bin/ntfs-automount"
	install -Dm644 "ntfs-automount@.service" "${DESTDIR}/usr/lib/systemd/system/ntfs-automount@.service"

uninstall:
	rm -f "${DESTDIR}/usr/lib/udev/rules.d/99-ntfs-automount.rules"
	rm -f "${DESTDIR}/usr/bin/ntfs-automount"
	rm -f "${DESTDIR}/usr/lib/systemd/system/ntfs-automount@.service"

.PHONY: all install uninstall

# .BEGIN is ignored by GNU make so we can use it as a guard
.BEGIN:
	@head -3 Makefile
	@false

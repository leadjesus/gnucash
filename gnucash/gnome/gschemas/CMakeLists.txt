
SET(gnome_GSCHEMA
  org.gnucash.dialogs.gschema.xml
  org.gnucash.dialogs.business.gschema.xml
  org.gnucash.dialogs.commodities.gschema.xml
  org.gnucash.dialogs.checkprinting.gschema.xml
  org.gnucash.dialogs.reconcile.gschema.xml
  org.gnucash.dialogs.sxs.gschema.xml
  org.gnucash.dialogs.totd.gschema.xml
  org.gnucash.gschema.xml
  org.gnucash.general.finance-quote.gschema.xml
  org.gnucash.window.pages.account.tree.gschema.xml
  org.gnucash.window.pages.gschema.xml
)

add_gschema_targets("${gnome_GSCHEMA}")

SET(gnome_gschema_DIST_local "")
FOREACH(file ${gnome_GSCHEMA})
    LIST(APPEND gnome_gschema_DIST_local ${file}.in.in)
ENDFOREACH()
SET_DIST_LIST(gnome_gschema_DIST CMakeLists.txt ${gnome_gschema_DIST_local})

========================
ApplicationDossier product Start and End dates follow ApplicationDossier Start and End dates
========================

Internal referencenumber: 6433

The validity of ApplicationDossier Products is automatically filled in according to the ApplicationDossier Start and End dates.

When initially adding a custom product, or products from a ProductGroup selection, the following rules apply:

    * The ApplicationProduct takes the StartDate of validity of a product (21_40_Product_IngangsdatumGeldigheid) from the ApplicationDossier field Dossier Startdate (16.40)
    * The ApplicationProduct takes the EndDate of validity of a product (21_41_Product_EinddatumGeldigheid) from the ApplicationDossier field Dossier Enddate (16.41)
    * The ApplicationProduct takes the "Necessary Until" date of a product ((21_60_Product_nodig_tot) from the ApplicationDossier field Dossier Enddate (16.41)
    * The user is allowed to manually overwrite the automatically filled in Start and End dates per product


Locations: 

* URL/Aanvraagdossier.aspx

Step-by-step:
n/a



# FAQ - Features - Geocoding

## When and how does SEED geocode my data?

SEED will attempt to geocode your data with latitude and longitude values only if the following are true:

1. Your organization has a MapQuest API key. You can register for one through [MapQuest's website](https://developer.mapquest.com/plan_purchase/steps/business_edition/business_edition_free/register) and apply it on your organization settings page.
2. The records being geocoded have address values that can be read by SEED. In your organization column settings page, you can specify which fields and in what order SEED will use to build the full address that will be geocoded by MapQuest.
3. The records being geocoded _do not_ already have latitude and longitude populated. SEED won't override these values, but you can edit and remove these values if you want SEED to attempt to generate them with MapQuest.

SEED will make this attempt in the following cases:

* During the file import process, after you've mapped columns, SEED will automatically attempt geocoding on records.

* On either the properties page or the tax lots page, you can select records and "Geocode Selected".

Note: Valid UBID (properties) or ULID (tax lots) values provide a latitude and longitude, and these can be used to provide latitude and longitude values. On import, UBID/ULID is used instead of MapQuest if available. On the inventory pages, there's a separate button to Decode UBID/ULID for Selected.

## I just geocoded my data using SEED. How do I review and verify the results?

There are multiple ways to do this. The most obvious way is to verify that latitude and longitude fields are populated. Additionally, SEED provides a field called "Geocoding Confidence". This field can provide evidence of how the geocoding went for that record - a value starting with "Low..." indicates that geocoding failed for a record because the address values didn't yield reliable results. Finally, SEED provides an inventory map page that allows you to view where the points are located on a map.

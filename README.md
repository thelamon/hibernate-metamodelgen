# Hibernate JPA 2 Metamodel Generator, forked

----

This fork fixes one simple issue in original metamodel generator - random order of fields in generated sources.

So, i added trivial sort order - id first (if present), all other fields are sorted alphabetically next to id:

	public static volatile SingularAttribute<SomeEntity, Integer> id;
	public static volatile SingularAttribute<SomeEntity, Date> beginDate;
	public static volatile SingularAttribute<SomeEntity, Date> endDate;
	public static volatile SingularAttribute<SomeEntity, Boolean> activeFlag;
	....

Works for me ^

----

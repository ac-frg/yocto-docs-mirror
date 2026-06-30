Azure Storage Shared Access Signature, when using the
:ref:`Azure Storage fetcher (az://) <bitbake-user-manual/bitbake-user-manual-fetching:fetchers>`
This variable can be defined to be used by the fetcher to authenticate
and gain access to non-public artifacts::

   AZ_SAS = ""se=2021-01-01&sp=r&sv=2018-11-09&sr=c&skoid=<skoid>&sig=<signature>""

For more information see Microsoft's Azure Storage documentation at
https://docs.microsoft.com/en-us/azure/storage/common/storage-sas-overview

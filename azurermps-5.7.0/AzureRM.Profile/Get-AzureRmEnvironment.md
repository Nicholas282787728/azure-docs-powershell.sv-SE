---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
ms.openlocfilehash: ac2ac931929acee527c900071de3062c4ef5398d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581059"
---
# Get-AzureRmEnvironment

## Sammanfattning
Hämta slut punkter och metadata för en instans av Azure-tjänster.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Med Get-AzureRmEnvironment cmdlet får du slut punkter och metadata för en instans av Azure-tjänsterna.

## BESKRIVS

### Exempel 1: skaffa AzureCloud-miljön
```
PS C:\> Get-AzureRmEnvironment AzureCloud

Name                                              : AzureCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.windows.net/
AdTenant                                          :
GalleryUrl                                        : https://gallery.azure.com/
ManagementPortalUrl                               : https://go.microsoft.com/fwlink/?LinkId=254433
ServiceManagementUrl                              : https://management.core.windows.net/
PublishSettingsFileUrl                            : https://go.microsoft.com/fwlink/?LinkID=301775
ResourceManagerUrl                                : https://management.azure.com/
SqlDatabaseDnsSuffix                              : .database.windows.net
StorageEndpointSuffix                             : core.windows.net
ActiveDirectoryAuthority                          : https://login.microsoftonline.com/
GraphUrl                                          : https://graph.windows.net/
GraphEndpointResourceId                           : https://graph.windows.net/
TrafficManagerDnsSuffix                           : trafficmanager.net
AzureKeyVaultDnsSuffix                            : vault.azure.net
AzureDataLakeStoreFileSystemEndpointSuffix        : azuredatalakestore.net
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix : azuredatalakeanalytics.net
AzureKeyVaultServiceEndpointResourceId            : https://vault.azure.net
```

Det här exemplet visar hur du kan hämta slut punkter och metadata för AzureCloud (standard).

### Exempel 2: skaffa AzureChinaCloud-miljön
```
PS C:\> Get-AzureRmEnvironment AzureChinaCloud

Name                                              : AzureChinaCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.chinacloudapi.cn/
AdTenant                                          :
GalleryUrl                                        : https://gallery.chinacloudapi.cn/
ManagementPortalUrl                               : https://go.microsoft.com/fwlink/?LinkId=301902
ServiceManagementUrl                              : https://management.core.chinacloudapi.cn/
PublishSettingsFileUrl                            : https://go.microsoft.com/fwlink/?LinkID=301776
ResourceManagerUrl                                : https://management.chinacloudapi.cn/
SqlDatabaseDnsSuffix                              : .database.chinacloudapi.cn
StorageEndpointSuffix                             : core.chinacloudapi.cn
ActiveDirectoryAuthority                          : https://login.chinacloudapi.cn/
GraphUrl                                          : https://graph.chinacloudapi.cn/
GraphEndpointResourceId                           : https://graph.chinacloudapi.cn/
TrafficManagerDnsSuffix                           : trafficmanager.cn
AzureKeyVaultDnsSuffix                            : vault.azure.cn
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            : https://vault.azure.cn
```

Det här exemplet visar hur du kan hämta slut punkter och metadata för AzureChinaCloud-miljön.

### Exempel 3: skaffa AzureUSGovernment-miljön
```
PS C:\> Get-AzureRmEnvironment AzureUSGovernment

Name                                              : AzureUSGovernment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.usgovcloudapi.net/
AdTenant                                          :
GalleryUrl                                        : https://gallery.usgovcloudapi.net/
ManagementPortalUrl                               : https://manage.windowsazure.us
ServiceManagementUrl                              : https://management.core.usgovcloudapi.net/
PublishSettingsFileUrl                            : https://manage.windowsazure.us/publishsettings/index
ResourceManagerUrl                                : https://management.usgovcloudapi.net/
SqlDatabaseDnsSuffix                              : .database.usgovcloudapi.net
StorageEndpointSuffix                             : core.usgovcloudapi.net
ActiveDirectoryAuthority                          : https://login.microsoftonline.us/
GraphUrl                                          : https://graph.windows.net/
GraphEndpointResourceId                           : https://graph.windows.net/
TrafficManagerDnsSuffix                           : usgovtrafficmanager.net
AzureKeyVaultDnsSuffix                            : vault.usgovcloudapi.net
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            : https://vault.usgovcloudapi.net
```

Det här exemplet visar hur du kan hämta slut punkter och metadata för AzureUSGovernment-miljön.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger namnet på Azure-instansen som ska visas.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### PSAzureEnvironment

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureRMEnvironment](./Add-AzureRMEnvironment.md)

[Remove-AzureRMEnvironment](./Remove-AzureRMEnvironment.md)

[Set-AzureRMEnvironment](./Set-AzureRMEnvironment.md)


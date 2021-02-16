---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
ms.openlocfilehash: 32e3bc6419ef94b177a06735654844d09ea04f3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226566"
---
# New-AzApiManagement

## SYNOPSIS
Skapar en API-hanteringsdistribution.

## SYNTAX

```
New-AzApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>]
 [-SslSetting <PsApiManagementSslSetting>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String[]>]
 [-EnableClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Den **nya cmdleten AzApiManagement** skapar en API-hanteringsdistribution i Azure API Management.

## EXEMPEL

### Exempel 1: Skapa en api-hanteringstjänst på utvecklarnivå
```powershell
PS D:\> New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi2" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"


PublicIPAddresses                     : {104.43.240.65}
PrivateIPAddresses                    :
Id                                    : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/ContosoGroup02/providers/Microsoft.ApiManagement/service/ContosoApi2
Name                                  : ContosoApi2
Location                              : Central US
Sku                                   : Developer
Capacity                              : 1
CreatedTimeUtc                        : 2/24/2020 10:34:12 PM
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://contosoapi2.azure-api.net
RuntimeRegionalUrl                    : https://contosoapi2-centralus-01.regional.azure-api.net
PortalUrl                             : https://contosoapi2.portal.azure-api.net
DeveloperPortalUrl                    : https://contosoapi2.developer.azure-api.net
ManagementApiUrl                      : https://contosoapi2.management.azure-api.net
ScmUrl                                : https://contosoapi2.scm.azure-api.net
PublisherEmail                        : admin@contoso.com
OrganizationName                      : Contoso
NotificationSenderEmail               : apimgmt-noreply@mail.windowsazure.com
VirtualNetwork                        :
VpnType                               : None
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {contosoapi2.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              :
EnableClientCertificate               :
ResourceGroupName                     : ContosoGroup02
```

Det här kommandot skapar en tjänst för hantering av utvecklar-API-nivå.
Kommandot anger organisationen och administratörsadressen.
Kommandot anger inte *SKU-parametern.*
Därför använder cmdleten standardvärdet Utvecklare.

### Exempel 2: Skapa en standardnivåtjänst som har tre enheter
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

Det här kommandot skapar en tjänst för hantering av standard-API som har tre enheter.

### Exempel 3: Skapa en förbrukningsnivåtjänst
```powershell
PS D:\github\azure-powershell> New-AzApiManagement -ResourceGroupName Api-Default-North-Europe -Name consumptionskuservice -Location 'West Europe' -Sku Consumption -Organization microsoft -AdminEmail contoso@contoso.com -SystemAssignedIdentity -EnableClientCertificate

PublicIPAddresses                     :
PrivateIPAddresses                    :
Id                                    : /subscriptions/subid/resourceGroups/Api-Default-North-Europe/providers/Microsoft.ApiManagement/service/consumptionskuservice
Name                                  : consumptionskuservice
Location                              : West Europe
Sku                                   : Consumption
Capacity                              : 0
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://consumptionskuservice.azure-api.net
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {consumptionskuservice.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity
EnableClientCertificate               : True
ResourceGroupName                     : Api-Default-North-Europe
```

Det här kommandot skapar en förbrukningsnivå-API-hanteringstjänst med Klientcertifikat aktiverat i Västeuropa.

### Exempel 4: Skapa en API-hanteringstjänst för ett externt virtuellt nätverk
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

Det här kommandot skapar en API-hanteringstjänst på premiumnivå i ett virtuellt Azure-nätverksundernät med en extern gatewayslutpunkt med en huvudregion i Usa.

### Exempel 5: Skapa en API-hanteringstjänst för ett internt virtuellt nätverk
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

Det här kommandot skapar en API-hanteringstjänst på premiumnivå i ett Virtuellt Azure-nätverksundernät med en intern gatewayslutpunkt med en huvudregion i Usa.

### Exempel 6: Skapa en API-hanteringstjänst och aktivera TLS 1.0-protokollet
```powershell
PS C:\> $enableTls=@{"Tls10" = "True"}
PS C:\> $sslSetting = New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls
PS C:\> New-AzApiManagement -ResourceGroupName Api-Default-CentralUS -Name "testtlspowershell" -Sku Standard -Location "CentralUS" -Organization "Microsoft" -AdminEmail "bar@contoso.com" -SslSetting $sslSetting

PublicIPAddresses                     : {23.99.140.18}
PrivateIPAddresses                    :
Id                                    : /subscriptions/subid/resourceGroups/Api-Default-CentralUS/providers/Microsoft.ApiManagement/service/testtlspowershell
Name                                  : testtlspowershell
Location                              : Central US
Sku                                   : Standard
Capacity                              : 1
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://testtlspowershell.azure-api.net
RuntimeRegionalUrl                    : https://testtlspowershell-centralus-01.regional.azure-api.net
PortalUrl                             : https://testtlspowershell.portal.azure-api.net
ManagementApiUrl                      : https://testtlspowershell.management.azure-api.net
ScmUrl                                : https://testtlspowershell.scm.azure-api.net
PublisherEmail                        : bar@contoso.com
OrganizationName                      : Microsoft
NotificationSenderEmail               : apimgmt-noreply@mail.windowsazure.com
VirtualNetwork                        :
VpnType                               : None
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {testtlspowershell.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              :
EnableClientCertificate               :
ResourceGroupName                     : Api-Default-CentralUS
```

Det här kommandot skapar en standard-SKU Api Management-tjänst och aktiverar TLS 1.0 på Klient klient på Klientsida till ApiManagement-gateway och Backend-klient mellan ApiManagement Gateway och Backend.

## PARAMETERS

### -AdditionalRegions
Ytterligare distributionsområden i Azure API Management.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminEmail
Anger den ursprungliga e-postadressen för alla meddelanden som API Management System skickar.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Kapacitet
Anger SKU-kapaciteten för Azure API-hanteringstjänsten.
Standardvärdet är ett (1).

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomHostnameConfiguration
Anpassade värdnamnskonfigurationer. Standardvärdet är $null. Passerar $null anger standardvärdnamnet.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableClientCertificate
Flagga endast avsedd att användas för SKU ApiManagement-tjänst för förbrukning. Detta framtvingar att ett klientcertifikat presenteras för varje begäran till gatewayen. Det här gör det också möjligt att autentisera certifikatet i principen på gatewayen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plats
Anger platsen där api-hanteringstjänsten ska skapas.
För att få giltiga platser använder du cmdleten Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | där {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object platser

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Anger ett namn för API-hanteringsdistributionen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Organisation
Anger namnet på en organisation.
API-hantering använder den här adressen i utvecklarportalen i e-postaviseringar.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resursgrupp där den här cmdleten skapar en API Management-distribution.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Anger nivån för API-hanteringstjänsten.
Giltiga värden är: 
- Utvecklare 
- Standard 
- Premium Standard är Utvecklare.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Basic, Standard, Premium, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SslSetting
Ssl-inställningen för ApiManagement-tjänsten. Standardvärdet är $null

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SystemAssignedIdentity
Generera och tilldela en Azure Active Directory-identitet för den här servern för användning med viktiga hanteringstjänster som Azure KeyVault.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SystemCertificateConfiguration
Certifikat som utfärdats av den interna certifikatutfärdaren för att installeras i tjänsten. Standardvärdet är $null.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Ordlista med flaggor.

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserAssignedIdentity
Tilldela den här servern användaridentiteter för användning med viktiga hanteringstjänster som Azure KeyVault.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
Virtuell nätverkskonfiguration av huvuddistributionsområdet för Azure API Management.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VpnType
Virtuell nätverkstyp för ApiManagement-distributionen. Giltiga värden är 
- "Inget" (standardvärde. ApiManagement ingår inte i något virtuellt nätverk")
- "Extern" (ApiManagement-distribution är konfigurerad i ett virtuellt nätverk med en slutpunkt mot Internet)
- "Internt" (ApiManagement-distribution är konfigurerad i ett virtuellt nätverk med en slutpunkt på intranätet)

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: (All)
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

### System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork

### System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]

## UTDATA

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Backup-AzapiManagement](./Backup-AzApiManagement.md)

[Get-AzapiManagement](./Get-AzApiManagement.md)

[Set-AzapiManagement](./Set-AzApiManagement.md)

[Remove-AzapiManagement](./Remove-AzApiManagement.md)

[Restore-AzapiManagement](./Restore-AzApiManagement.md)



---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
ms.openlocfilehash: 01e4e6b990a35b8573a9ea1d2f2803f6d6fabc1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581351"
---
# Get-AzureRmResource

## Sammanfattning
Hämtar resurser.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### Parametern lista alla resurser. Vis
```
Get-AzureRmResource [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Skaffa en enda resurs utifrån dess ID.
```
Get-AzureRmResource -ResourceId <String> [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Skaffa en enda resurs på klient organisations nivå.
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Visar de resurser som baseras på den angivna omfattningen på klient organisations nivå.
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-Top <Int32>] [-ODataQuery <String>]
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Hämta resurs utifrån namn och grupp
```
Get-AzureRmResource [-ResourceName <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Skaffa en resurs via namn och typ.
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Hämta resurs efter namn, grupp och typ
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-ODataQuery <String>] -ResourceGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Skaffa resurs samling
```
Get-AzureRmResource [-ResourceType <String>] [-ExtensionResourceType <String>] [-ExpandProperties]
 [-IsCollection] [-ODataQuery <String>] [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmResource** får Azure-resurser.

## BESKRIVS

### Exempel 1: skaffa en resurs
```
PS C:\>Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoWebsite"
```

Det här kommandot får en resurs av typen Microsoft. Web/Sites, med namnet ContosoWebsite under ResourceGroup11.

## MALLPARAMETRAR

### -ApiVersion
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpandProperties
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

### -ExtensionResourceName
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource by name, group and type
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ExtensionResourceType
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource by name, group and type
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IsCollection
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ODataQuery
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -För
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

### -ResourceGroupName
```yaml
Type: System.String
Parameter Sets: Get resource by name and group
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource by name, group and type
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Anger fullständigt resurs-ID, inklusive prenumerationen, som i följande exempel: 

`/subscriptions/`abonnemangs-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`

Denna cmdlet tar resursen med detta ID.

```yaml
Type: System.String
Parameter Sets: Get a single resource by its Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceName
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Get resource by name, group and type
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type.
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceType
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Get resource by name, group and type
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get a resource by name and type.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantLevel
Anger att denna cmdlet fungerar på klient nivån.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Överst
```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### System. Management. Automation. PSObject

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Sök-AzureRmResource](./Find-AzureRmResource.md)

[Move-AzureRmResource](./Move-AzureRmResource.md)

[New-AzureRmResource](./New-AzureRmResource.md)

[Remove-AzureRmResource](./Remove-AzureRmResource.md)

[Set-AzureRmResource](./Set-AzureRmResource.md)



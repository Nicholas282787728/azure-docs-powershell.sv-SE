---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFB0000C-2EFF-4216-923B-55B0B07BFE60
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51ab7d137fbbac1925ae689a1dcb16c89b9b8000
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093332"
---
# <span data-ttu-id="fc02d-101">Get-AzureServiceAvailableExtension</span><span class="sxs-lookup"><span data-stu-id="fc02d-101">Get-AzureServiceAvailableExtension</span></span>

## <span data-ttu-id="fc02d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fc02d-102">SYNOPSIS</span></span>
<span data-ttu-id="fc02d-103">Hämtar information om de tillgängliga tilläggen för värd tjänster.</span><span class="sxs-lookup"><span data-stu-id="fc02d-103">Gets information about the available extensions for hosted services.</span></span>

## <span data-ttu-id="fc02d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fc02d-104">SYNTAX</span></span>

### <span data-ttu-id="fc02d-105">ListLatestExtensions (standard)</span><span class="sxs-lookup"><span data-stu-id="fc02d-105">ListLatestExtensions (Default)</span></span>
```
Get-AzureServiceAvailableExtension [[-ExtensionName] <String>] [[-ProviderNamespace] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc02d-106">ListAllVersions</span><span class="sxs-lookup"><span data-stu-id="fc02d-106">ListAllVersions</span></span>
```
Get-AzureServiceAvailableExtension [-ExtensionName] <String> [-ProviderNamespace] <String> [-AllVersions]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc02d-107">ListSingleVersion</span><span class="sxs-lookup"><span data-stu-id="fc02d-107">ListSingleVersion</span></span>
```
Get-AzureServiceAvailableExtension [-ExtensionName] <String> [-ProviderNamespace] <String> [-Version] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc02d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fc02d-108">DESCRIPTION</span></span>
<span data-ttu-id="fc02d-109">Cmdleten **Get-AzureServiceAvailableExtension** hämtar information för de senaste tillgängliga tilläggen för värdbaserade tjänster.</span><span class="sxs-lookup"><span data-stu-id="fc02d-109">The **Get-AzureServiceAvailableExtension** cmdlet gets information for the latest available extensions for hosted services.</span></span>

## <span data-ttu-id="fc02d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fc02d-110">EXAMPLES</span></span>

### <span data-ttu-id="fc02d-111">Exempel 1: Hämta tillgängliga tillägg</span><span class="sxs-lookup"><span data-stu-id="fc02d-111">Example 1: Get available extensions</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="fc02d-112">Det här kommandot får alla tillgängliga tillägg.</span><span class="sxs-lookup"><span data-stu-id="fc02d-112">This command gets all available extensions.</span></span>

### <span data-ttu-id="fc02d-113">Exempel 2: Hämta tillägg i ett angivet namn område</span><span class="sxs-lookup"><span data-stu-id="fc02d-113">Example 2: Get extensions in a specified namespace</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension -ProviderNamespace Microsoft.Windows.Azure.Extensions -ExtensionName "RDP" -AllVersions

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0.0.1
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="fc02d-114">Med det här kommandot får du fil namns tilläggen med ett angivet namn i ett angivet namn område.</span><span class="sxs-lookup"><span data-stu-id="fc02d-114">This command gets the extensions with a specified name in a specified namespace.</span></span>

### <span data-ttu-id="fc02d-115">Exempel 3: skaffa en specifik version av ett tillägg</span><span class="sxs-lookup"><span data-stu-id="fc02d-115">Example 3: Get a specific version of an extension</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension -ProviderNamespace Microsoft.Windows.Azure.Extensions -ExtensionName "RDP" -Version 1.0.0.1

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0.0.1
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="fc02d-116">Det här kommandot får information om en viss version av ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="fc02d-116">This command gets information about a specific version of an extension.</span></span>

## <span data-ttu-id="fc02d-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fc02d-117">PARAMETERS</span></span>

### <span data-ttu-id="fc02d-118">-AllVersions</span><span class="sxs-lookup"><span data-stu-id="fc02d-118">-AllVersions</span></span>
<span data-ttu-id="fc02d-119">Anger att denna cmdlet får alla versioner av ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="fc02d-119">Indicates that this cmdlet gets all versions of an extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAllVersions
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc02d-120">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="fc02d-120">-ExtensionName</span></span>
<span data-ttu-id="fc02d-121">Anger tillägget.</span><span class="sxs-lookup"><span data-stu-id="fc02d-121">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: ListLatestExtensions
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListAllVersions, ListSingleVersion
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc02d-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="fc02d-122">-InformationAction</span></span>
<span data-ttu-id="fc02d-123">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="fc02d-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fc02d-124">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="fc02d-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fc02d-125">Vidare</span><span class="sxs-lookup"><span data-stu-id="fc02d-125">Continue</span></span>
- <span data-ttu-id="fc02d-126">Över</span><span class="sxs-lookup"><span data-stu-id="fc02d-126">Ignore</span></span>
- <span data-ttu-id="fc02d-127">Inquire</span><span class="sxs-lookup"><span data-stu-id="fc02d-127">Inquire</span></span>
- <span data-ttu-id="fc02d-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fc02d-128">SilentlyContinue</span></span>
- <span data-ttu-id="fc02d-129">Stanna</span><span class="sxs-lookup"><span data-stu-id="fc02d-129">Stop</span></span>
- <span data-ttu-id="fc02d-130">Avbryt</span><span class="sxs-lookup"><span data-stu-id="fc02d-130">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc02d-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fc02d-131">-InformationVariable</span></span>
<span data-ttu-id="fc02d-132">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="fc02d-132">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc02d-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="fc02d-133">-Profile</span></span>
<span data-ttu-id="fc02d-134">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="fc02d-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fc02d-135">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="fc02d-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc02d-136">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="fc02d-136">-ProviderNamespace</span></span>
<span data-ttu-id="fc02d-137">Anger namn området för tilläggs leverantör.</span><span class="sxs-lookup"><span data-stu-id="fc02d-137">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: ListLatestExtensions
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListAllVersions, ListSingleVersion
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc02d-138">-Version</span><span class="sxs-lookup"><span data-stu-id="fc02d-138">-Version</span></span>
<span data-ttu-id="fc02d-139">Anger tilläggs versionen.</span><span class="sxs-lookup"><span data-stu-id="fc02d-139">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: ListSingleVersion
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc02d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc02d-140">CommonParameters</span></span>
<span data-ttu-id="fc02d-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc02d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc02d-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc02d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc02d-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fc02d-143">INPUTS</span></span>

## <span data-ttu-id="fc02d-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fc02d-144">OUTPUTS</span></span>

## <span data-ttu-id="fc02d-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fc02d-145">NOTES</span></span>

## <span data-ttu-id="fc02d-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fc02d-146">RELATED LINKS</span></span>

[<span data-ttu-id="fc02d-147">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="fc02d-147">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)



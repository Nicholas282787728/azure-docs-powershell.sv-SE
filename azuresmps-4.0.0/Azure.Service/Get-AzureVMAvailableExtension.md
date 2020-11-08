---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FAC3DABB-8230-4E86-9936-0F1848980EA2
online version: ''
schema: 2.0.0
ms.openlocfilehash: d062b4300af2efbd45bfccd7ed467871b23d8256
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099774"
---
# <span data-ttu-id="93c49-101">Get-AzureVMAvailableExtension</span><span class="sxs-lookup"><span data-stu-id="93c49-101">Get-AzureVMAvailableExtension</span></span>

## <span data-ttu-id="93c49-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="93c49-102">SYNOPSIS</span></span>
<span data-ttu-id="93c49-103">Hämtar information för de senaste tillgängliga tilläggen för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="93c49-103">Gets information for the latest available extensions for virtual machines.</span></span>

## <span data-ttu-id="93c49-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="93c49-104">SYNTAX</span></span>

### <span data-ttu-id="93c49-105">ListLatestExtensions (standard)</span><span class="sxs-lookup"><span data-stu-id="93c49-105">ListLatestExtensions (Default)</span></span>
```
Get-AzureVMAvailableExtension [[-ExtensionName] <String>] [[-Publisher] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="93c49-106">ListAllVersions</span><span class="sxs-lookup"><span data-stu-id="93c49-106">ListAllVersions</span></span>
```
Get-AzureVMAvailableExtension [-ExtensionName] <String> [-Publisher] <String> [-AllVersions]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="93c49-107">ListSingleVersion</span><span class="sxs-lookup"><span data-stu-id="93c49-107">ListSingleVersion</span></span>
```
Get-AzureVMAvailableExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="93c49-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="93c49-108">DESCRIPTION</span></span>
<span data-ttu-id="93c49-109">Cmdleten **Get-AzureVMAvailableExtension** hämtar information för de senaste tillgängliga tilläggen för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="93c49-109">The **Get-AzureVMAvailableExtension** cmdlet gets information for the latest available extensions for virtual machines.</span></span>

## <span data-ttu-id="93c49-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="93c49-110">EXAMPLES</span></span>

### <span data-ttu-id="93c49-111">Exempel 1: få information om de senaste tilläggen</span><span class="sxs-lookup"><span data-stu-id="93c49-111">Example 1: Get information for the latest available extensions</span></span>
```
PS C:\> Get-AzureVMAvailableExtension
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="93c49-112">Med det här kommandot får du information om de senaste tillgängliga tilläggen för alla virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="93c49-112">This command gets information for the latest available extensions for all virtual machines.</span></span>

### <span data-ttu-id="93c49-113">Exempel 2: Hämta information från ett angivet tilläggs namn</span><span class="sxs-lookup"><span data-stu-id="93c49-113">Example 2: Get information from a specified extension name</span></span>
```
PS C:\> Get-AzureVMAvailableExtension -Publisher Microsoft.Compute -ExtensionName "VMAccessAgent" -AllVersions
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.2
          PublicConfigurationSchema  : 
          <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>

          PrivateConfigurationSchema : 
          <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>

          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded

          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.3
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="93c49-114">Med det här kommandot får du information från alla versioner av tillägget som heter VMAccessAgent och utgivaren med namnet Microsoft. Computer.</span><span class="sxs-lookup"><span data-stu-id="93c49-114">This command gets information from all versions of the extension named VMAccessAgent and the publisher named Microsoft.Computer.</span></span>

### <span data-ttu-id="93c49-115">Exempel 3: Hämta information från ett visst virtuellt dator tillägg med versions nummer</span><span class="sxs-lookup"><span data-stu-id="93c49-115">Example 3: Get information from a specific virtual machine extension by version number</span></span>
```
PS C:\> Get-AzureVMAvailableExtension -Publisher Microsoft.Compute -ExtensionName VMAccessAgent -Version 1.0.3
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.3
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="93c49-116">Med det här kommandot får du information om tillägget VMAccessAgent och utgivaren med namnet Microsoft. Compute för versions hanterings versionen 1.0.3.</span><span class="sxs-lookup"><span data-stu-id="93c49-116">This command gets information for the extension named VMAccessAgent and the publisher named Microsoft.Compute for the extension version 1.0.3.</span></span>

## <span data-ttu-id="93c49-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="93c49-117">PARAMETERS</span></span>

### <span data-ttu-id="93c49-118">-AllVersions</span><span class="sxs-lookup"><span data-stu-id="93c49-118">-AllVersions</span></span>
<span data-ttu-id="93c49-119">Anger att denna cmdlet visar alla versioner av ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="93c49-119">Indicates that this cmdlet lists all versions of an extension.</span></span>

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

### <span data-ttu-id="93c49-120">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="93c49-120">-ExtensionName</span></span>
<span data-ttu-id="93c49-121">Anger namnet på det tillgängliga tillägget.</span><span class="sxs-lookup"><span data-stu-id="93c49-121">Specifies the name of the available extension.</span></span>

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

### <span data-ttu-id="93c49-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="93c49-122">-InformationAction</span></span>
<span data-ttu-id="93c49-123">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="93c49-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="93c49-124">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="93c49-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="93c49-125">Vidare</span><span class="sxs-lookup"><span data-stu-id="93c49-125">Continue</span></span>
- <span data-ttu-id="93c49-126">Över</span><span class="sxs-lookup"><span data-stu-id="93c49-126">Ignore</span></span>
- <span data-ttu-id="93c49-127">Inquire</span><span class="sxs-lookup"><span data-stu-id="93c49-127">Inquire</span></span>
- <span data-ttu-id="93c49-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="93c49-128">SilentlyContinue</span></span>
- <span data-ttu-id="93c49-129">Stanna</span><span class="sxs-lookup"><span data-stu-id="93c49-129">Stop</span></span>
- <span data-ttu-id="93c49-130">Avbryt</span><span class="sxs-lookup"><span data-stu-id="93c49-130">Suspend</span></span>

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

### <span data-ttu-id="93c49-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="93c49-131">-InformationVariable</span></span>
<span data-ttu-id="93c49-132">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="93c49-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="93c49-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="93c49-133">-Profile</span></span>
<span data-ttu-id="93c49-134">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="93c49-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="93c49-135">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="93c49-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="93c49-136">-Publisher</span><span class="sxs-lookup"><span data-stu-id="93c49-136">-Publisher</span></span>
<span data-ttu-id="93c49-137">Anger utgivaren av tillägget.</span><span class="sxs-lookup"><span data-stu-id="93c49-137">Specifies the publisher of the extension.</span></span>

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

### <span data-ttu-id="93c49-138">-Version</span><span class="sxs-lookup"><span data-stu-id="93c49-138">-Version</span></span>
<span data-ttu-id="93c49-139">Anger version för tillägget.</span><span class="sxs-lookup"><span data-stu-id="93c49-139">Specifies the version of the extension.</span></span>

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

### <span data-ttu-id="93c49-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93c49-140">CommonParameters</span></span>
<span data-ttu-id="93c49-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93c49-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93c49-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93c49-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93c49-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="93c49-143">INPUTS</span></span>

## <span data-ttu-id="93c49-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="93c49-144">OUTPUTS</span></span>

## <span data-ttu-id="93c49-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="93c49-145">NOTES</span></span>

## <span data-ttu-id="93c49-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="93c49-146">RELATED LINKS</span></span>


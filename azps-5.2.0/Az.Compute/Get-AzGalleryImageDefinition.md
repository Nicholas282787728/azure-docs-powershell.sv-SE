---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
ms.openlocfilehash: c6c689ce2c9ccda71150f221bdea4ae5dd2a20fc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392952"
---
# <span data-ttu-id="38a2b-101">Get-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="38a2b-101">Get-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="38a2b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="38a2b-102">SYNOPSIS</span></span>
<span data-ttu-id="38a2b-103">Bild definitionerna hämta eller lista Galleri.</span><span class="sxs-lookup"><span data-stu-id="38a2b-103">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="38a2b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="38a2b-104">SYNTAX</span></span>

### <span data-ttu-id="38a2b-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="38a2b-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38a2b-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="38a2b-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageDefinition [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38a2b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="38a2b-107">DESCRIPTION</span></span>
<span data-ttu-id="38a2b-108">Bild definitionerna hämta eller lista Galleri.</span><span class="sxs-lookup"><span data-stu-id="38a2b-108">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="38a2b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="38a2b-109">EXAMPLES</span></span>

### <span data-ttu-id="38a2b-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="38a2b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="38a2b-111">Hämta bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="38a2b-111">Get the gallery image definition.</span></span>

### <span data-ttu-id="38a2b-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="38a2b-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image*

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image2
Name                : image2
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="38a2b-113">Hämta bild definitionen för galleriet som börjar med "bild".</span><span class="sxs-lookup"><span data-stu-id="38a2b-113">Get the gallery image definition that starts with "image".</span></span>

### <span data-ttu-id="38a2b-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="38a2b-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image2
Name                : image2
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="38a2b-115">Hämta bild definitionerna för galleriet i gallery1.</span><span class="sxs-lookup"><span data-stu-id="38a2b-115">Get the gallery image definitions in gallery1.</span></span>

## <span data-ttu-id="38a2b-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="38a2b-116">PARAMETERS</span></span>

### <span data-ttu-id="38a2b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38a2b-117">-DefaultProfile</span></span>
<span data-ttu-id="38a2b-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="38a2b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38a2b-119">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="38a2b-119">-GalleryName</span></span>
<span data-ttu-id="38a2b-120">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="38a2b-120">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38a2b-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="38a2b-121">-Name</span></span>
<span data-ttu-id="38a2b-122">Namnet på bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="38a2b-122">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="38a2b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38a2b-123">-ResourceGroupName</span></span>
<span data-ttu-id="38a2b-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="38a2b-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38a2b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38a2b-125">-ResourceId</span></span>
<span data-ttu-id="38a2b-126">Resurs-ID för bild definitionen för galleriet</span><span class="sxs-lookup"><span data-stu-id="38a2b-126">The resource ID for the gallery image definition</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38a2b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38a2b-127">CommonParameters</span></span>
<span data-ttu-id="38a2b-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38a2b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38a2b-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38a2b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38a2b-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="38a2b-130">INPUTS</span></span>

### <span data-ttu-id="38a2b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="38a2b-131">System.String</span></span>

## <span data-ttu-id="38a2b-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="38a2b-132">OUTPUTS</span></span>

### <span data-ttu-id="38a2b-133">Microsoft. Azure. commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="38a2b-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="38a2b-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="38a2b-134">NOTES</span></span>

## <span data-ttu-id="38a2b-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="38a2b-135">RELATED LINKS</span></span>

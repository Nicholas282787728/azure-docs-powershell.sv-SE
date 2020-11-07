---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
ms.openlocfilehash: 57c0a05c5b0f279fa7c9f06cd561385de87698bf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927654"
---
# <span data-ttu-id="fe6de-101">Update-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fe6de-101">Update-AzDataFactoryV2</span></span>

## <span data-ttu-id="fe6de-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe6de-102">SYNOPSIS</span></span>
<span data-ttu-id="fe6de-103">Uppdaterar egenskaperna för en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="fe6de-103">Updates the properties of a data factory.</span></span>

## <span data-ttu-id="fe6de-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe6de-104">SYNTAX</span></span>

### <span data-ttu-id="fe6de-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="fe6de-105">ByFactoryName (Default)</span></span>
```
Update-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe6de-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fe6de-106">ByFactoryObject</span></span>
```
Update-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe6de-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fe6de-107">ByResourceId</span></span>
```
Update-AzDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe6de-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe6de-108">DESCRIPTION</span></span>
<span data-ttu-id="fe6de-109">Cmdleten **Update-AzDataFactoryV2** uppdaterar märkningarna eller identitets egenskaperna för en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="fe6de-109">The **Update-AzDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="fe6de-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe6de-110">EXAMPLES</span></span>

### <span data-ttu-id="fe6de-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fe6de-111">Example 1</span></span>
```
PS C:\> Update-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Tag @{myNewTagName = "myTagValue"}

Confirm
Are you sure you want to update properties of the data factory 'WikiADF' in resource group 'ADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


DataFactoryName   : WikiADF
DataFactoryId     : /subscriptions/1e42591f-1f0c-4c5a-b7f2-a268f6105ec5/resourceGroups/adf/providers/Microsoft.DataF
                    actory/factories/wikiadf
ResourceGroupName : ADF
Location          : EastUS
Tags              : {[myNewTagName, myTagValue]}
Identity          :
ProvisioningState : Succeeded
```

<span data-ttu-id="fe6de-112">Det här kommandot uppdaterar taggarna för tillverknings WikiADF till en ord lista som innehåller en tagg med namnet myNewTagName med värdet myTagValue.</span><span class="sxs-lookup"><span data-stu-id="fe6de-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="fe6de-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe6de-113">PARAMETERS</span></span>

### <span data-ttu-id="fe6de-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe6de-114">-DefaultProfile</span></span>
<span data-ttu-id="fe6de-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fe6de-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe6de-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe6de-116">-InputObject</span></span>
<span data-ttu-id="fe6de-117">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="fe6de-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe6de-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="fe6de-118">-Name</span></span>
<span data-ttu-id="fe6de-119">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="fe6de-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6de-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe6de-120">-ResourceGroupName</span></span>
<span data-ttu-id="fe6de-121">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="fe6de-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6de-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe6de-122">-ResourceId</span></span>
<span data-ttu-id="fe6de-123">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="fe6de-123">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe6de-124">-Tagg</span><span class="sxs-lookup"><span data-stu-id="fe6de-124">-Tag</span></span>
<span data-ttu-id="fe6de-125">Taggarna för data fabriken.</span><span class="sxs-lookup"><span data-stu-id="fe6de-125">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6de-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fe6de-126">-Confirm</span></span>
<span data-ttu-id="fe6de-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fe6de-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6de-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe6de-128">-WhatIf</span></span>
<span data-ttu-id="fe6de-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fe6de-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe6de-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fe6de-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6de-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe6de-131">CommonParameters</span></span>
<span data-ttu-id="fe6de-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe6de-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe6de-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe6de-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe6de-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe6de-134">INPUTS</span></span>

### <span data-ttu-id="fe6de-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fe6de-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="fe6de-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fe6de-136">System.String</span></span>

## <span data-ttu-id="fe6de-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe6de-137">OUTPUTS</span></span>

### <span data-ttu-id="fe6de-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fe6de-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="fe6de-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe6de-139">NOTES</span></span>

## <span data-ttu-id="fe6de-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe6de-140">RELATED LINKS</span></span>

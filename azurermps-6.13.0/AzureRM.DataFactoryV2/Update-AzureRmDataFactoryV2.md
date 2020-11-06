---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2.md
ms.openlocfilehash: 09e13e973178444496604843336c8f483508c59e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577053"
---
# <span data-ttu-id="ffc40-101">Update-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ffc40-101">Update-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="ffc40-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ffc40-102">SYNOPSIS</span></span>
<span data-ttu-id="ffc40-103">Uppdaterar egenskaperna för en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="ffc40-103">Updates the properties of a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffc40-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ffc40-104">SYNTAX</span></span>

### <span data-ttu-id="ffc40-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="ffc40-105">ByFactoryName (Default)</span></span>
```
Update-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffc40-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ffc40-106">ByFactoryObject</span></span>
```
Update-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffc40-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ffc40-107">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffc40-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ffc40-108">DESCRIPTION</span></span>
<span data-ttu-id="ffc40-109">Cmdleten **Update-AzureRmDataFactoryV2** uppdaterar märkningarna eller identitets egenskaperna för en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="ffc40-109">The **Update-AzureRmDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="ffc40-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ffc40-110">EXAMPLES</span></span>

### <span data-ttu-id="ffc40-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ffc40-111">Example 1</span></span>
```
PS C:\> Update-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Tag @{myNewTagName = "myTagValue"}

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

<span data-ttu-id="ffc40-112">Det här kommandot uppdaterar taggarna för tillverknings WikiADF till en ord lista som innehåller en tagg med namnet myNewTagName med värdet myTagValue.</span><span class="sxs-lookup"><span data-stu-id="ffc40-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="ffc40-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ffc40-113">PARAMETERS</span></span>

### <span data-ttu-id="ffc40-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffc40-114">-DefaultProfile</span></span>
<span data-ttu-id="ffc40-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ffc40-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffc40-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ffc40-116">-InputObject</span></span>
<span data-ttu-id="ffc40-117">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="ffc40-117">The data factory object.</span></span>

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

### <span data-ttu-id="ffc40-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ffc40-118">-Name</span></span>
<span data-ttu-id="ffc40-119">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="ffc40-119">The data factory name.</span></span>

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

### <span data-ttu-id="ffc40-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffc40-120">-ResourceGroupName</span></span>
<span data-ttu-id="ffc40-121">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ffc40-121">The resource group name.</span></span>

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

### <span data-ttu-id="ffc40-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ffc40-122">-ResourceId</span></span>
<span data-ttu-id="ffc40-123">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="ffc40-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ffc40-124">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ffc40-124">-Tag</span></span>
<span data-ttu-id="ffc40-125">Taggarna för data fabriken.</span><span class="sxs-lookup"><span data-stu-id="ffc40-125">The tags of the data factory.</span></span>

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

### <span data-ttu-id="ffc40-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ffc40-126">-Confirm</span></span>
<span data-ttu-id="ffc40-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ffc40-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffc40-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffc40-128">-WhatIf</span></span>
<span data-ttu-id="ffc40-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ffc40-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ffc40-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ffc40-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffc40-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffc40-131">CommonParameters</span></span>
<span data-ttu-id="ffc40-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffc40-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffc40-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffc40-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffc40-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ffc40-134">INPUTS</span></span>

### <span data-ttu-id="ffc40-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ffc40-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="ffc40-136">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ffc40-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ffc40-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ffc40-137">System.String</span></span>

## <span data-ttu-id="ffc40-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ffc40-138">OUTPUTS</span></span>

### <span data-ttu-id="ffc40-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ffc40-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="ffc40-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ffc40-140">NOTES</span></span>

## <span data-ttu-id="ffc40-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ffc40-141">RELATED LINKS</span></span>

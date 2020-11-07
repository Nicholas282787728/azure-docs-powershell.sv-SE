---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2.md
ms.openlocfilehash: d7173b75d9796eeab974973f9f997d5b7cb72b49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756098"
---
# <span data-ttu-id="eb258-101">Update-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="eb258-101">Update-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="eb258-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb258-102">SYNOPSIS</span></span>
<span data-ttu-id="eb258-103">Uppdaterar egenskaperna för en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="eb258-103">Updates the properties of a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb258-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb258-104">SYNTAX</span></span>

### <span data-ttu-id="eb258-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="eb258-105">ByFactoryName (Default)</span></span>
```
Update-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb258-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="eb258-106">ByFactoryObject</span></span>
```
Update-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb258-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="eb258-107">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2 [-ResourceId] <String> [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb258-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb258-108">DESCRIPTION</span></span>
<span data-ttu-id="eb258-109">Cmdleten **Update-AzureRmDataFactoryV2** uppdaterar märkningarna eller identitets egenskaperna för en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="eb258-109">The **Update-AzureRmDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="eb258-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb258-110">EXAMPLES</span></span>

### <span data-ttu-id="eb258-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="eb258-111">Example 1</span></span>
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

<span data-ttu-id="eb258-112">Det här kommandot uppdaterar taggarna för tillverknings WikiADF till en ord lista som innehåller en tagg med namnet myNewTagName med värdet myTagValue.</span><span class="sxs-lookup"><span data-stu-id="eb258-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="eb258-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb258-113">PARAMETERS</span></span>

### <span data-ttu-id="eb258-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb258-114">-DefaultProfile</span></span>
<span data-ttu-id="eb258-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eb258-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb258-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb258-116">-InputObject</span></span>
<span data-ttu-id="eb258-117">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="eb258-117">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb258-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="eb258-118">-Name</span></span>
<span data-ttu-id="eb258-119">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="eb258-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb258-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb258-120">-ResourceGroupName</span></span>
<span data-ttu-id="eb258-121">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="eb258-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb258-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb258-122">-ResourceId</span></span>
<span data-ttu-id="eb258-123">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="eb258-123">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb258-124">-Tagg</span><span class="sxs-lookup"><span data-stu-id="eb258-124">-Tag</span></span>
<span data-ttu-id="eb258-125">Taggarna för data fabriken.</span><span class="sxs-lookup"><span data-stu-id="eb258-125">The tags of the data factory.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb258-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eb258-126">-Confirm</span></span>
<span data-ttu-id="eb258-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eb258-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb258-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb258-128">-WhatIf</span></span>
<span data-ttu-id="eb258-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eb258-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb258-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eb258-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb258-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb258-131">CommonParameters</span></span>
<span data-ttu-id="eb258-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb258-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb258-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb258-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb258-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb258-134">INPUTS</span></span>

### <span data-ttu-id="eb258-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="eb258-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="eb258-136">System. String Microsoft. Azure. Management. DataFactory. Models. FactoryIdentity</span><span class="sxs-lookup"><span data-stu-id="eb258-136">System.String Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity</span></span>

## <span data-ttu-id="eb258-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb258-137">OUTPUTS</span></span>

### <span data-ttu-id="eb258-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="eb258-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="eb258-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb258-139">NOTES</span></span>

## <span data-ttu-id="eb258-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb258-140">RELATED LINKS</span></span>


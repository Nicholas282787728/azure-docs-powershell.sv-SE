---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 8742babd73e28e28797db75952d7eb9e9c8dc4a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579712"
---
# <span data-ttu-id="5f3fc-101">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5f3fc-101">Get-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="5f3fc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f3fc-102">SYNOPSIS</span></span>
<span data-ttu-id="5f3fc-103">Hämtar information om data fabrik.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-103">Gets information about Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f3fc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f3fc-104">SYNTAX</span></span>

```
Get-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>]
```

## <span data-ttu-id="5f3fc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f3fc-105">DESCRIPTION</span></span>
<span data-ttu-id="5f3fc-106">Get-AzureRmDataFactoryV2-cmdleten får information om data fabrikerna i en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-106">The Get-AzureRmDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="5f3fc-107">Om du anger namnet på en data fabrik får denna cmdlet information om den data fabriken.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="5f3fc-108">Om du inte anger ett namn hämtas den här cmdleten information om alla data fabrikerna i en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>


## <span data-ttu-id="5f3fc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f3fc-109">EXAMPLES</span></span>

### <span data-ttu-id="5f3fc-110">Exempel 1: Hämta alla data fabriker</span><span class="sxs-lookup"><span data-stu-id="5f3fc-110">Example 1: Get all data factories</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

    DataFactoryName   : WikiADF2
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf2
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          :
    ProvisioningState : Succeeded

```

<span data-ttu-id="5f3fc-111">Visar information om alla data faktorer i Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-111">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="5f3fc-112">Exempel 2: skaffa en specifik data fabrik</span><span class="sxs-lookup"><span data-stu-id="5f3fc-112">Example 2: Get a specific data factory</span></span>
```
PS C:\> $DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

```

<span data-ttu-id="5f3fc-113">Det här kommandot visar information om data fabriken med namnet WikiADF i prenumerationen för resurs gruppen med namnet ADF och sedan lagras den i $DataFactory variabel.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="5f3fc-114">Ange parametern DataFactory i efterföljande cmdlets för att använda data fabriken som lagras i $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-114">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="5f3fc-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f3fc-115">PARAMETERS</span></span>

### <span data-ttu-id="5f3fc-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="5f3fc-116">-Name</span></span>
<span data-ttu-id="5f3fc-117">Anger namnet på data fabriken för att få information.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-117">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f3fc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f3fc-118">-ResourceGroupName</span></span>
<span data-ttu-id="5f3fc-119">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-119">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5f3fc-120">Denna cmdlet hämtar information om de data fabriker som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-120">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="5f3fc-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f3fc-121">INPUTS</span></span>

### <span data-ttu-id="5f3fc-122">System. String</span><span class="sxs-lookup"><span data-stu-id="5f3fc-122">System.String</span></span>


## <span data-ttu-id="5f3fc-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f3fc-123">OUTPUTS</span></span>

### <span data-ttu-id="5f3fc-124">System. Collections. Generic. list ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory, Microsoft. Azure. commands. DataFactoryV2, version = 0.1.9.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5f3fc-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="5f3fc-125">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5f3fc-125">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="5f3fc-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f3fc-126">NOTES</span></span>
<span data-ttu-id="5f3fc-127">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="5f3fc-127">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5f3fc-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f3fc-128">RELATED LINKS</span></span>
[<span data-ttu-id="5f3fc-129">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5f3fc-129">Set-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="5f3fc-130">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5f3fc-130">Remove-AzureRmDataFactoryV2</span></span>]()


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
ms.openlocfilehash: fac2e899984f9d626f6c7342043166649327a0f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321040"
---
# <span data-ttu-id="26799-101">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="26799-101">Get-AzDataFactoryV2</span></span>

## <span data-ttu-id="26799-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26799-102">SYNOPSIS</span></span>
<span data-ttu-id="26799-103">Hämtar information om data fabrik.</span><span class="sxs-lookup"><span data-stu-id="26799-103">Gets information about Data Factory.</span></span>

## <span data-ttu-id="26799-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26799-104">SYNTAX</span></span>

### <span data-ttu-id="26799-105">BySubscriptionId (standard)</span><span class="sxs-lookup"><span data-stu-id="26799-105">BySubscriptionId (Default)</span></span>
```
Get-AzDataFactoryV2 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26799-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="26799-106">ByFactoryName</span></span>
```
Get-AzDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26799-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26799-107">DESCRIPTION</span></span>
<span data-ttu-id="26799-108">Get-AzDataFactoryV2-cmdleten får information om data fabrikerna i en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="26799-108">The Get-AzDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="26799-109">Om du anger namnet på en data fabrik får denna cmdlet information om den data fabriken.</span><span class="sxs-lookup"><span data-stu-id="26799-109">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="26799-110">Om du inte anger ett namn hämtas den här cmdleten information om alla data fabrikerna i en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="26799-110">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="26799-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26799-111">EXAMPLES</span></span>

### <span data-ttu-id="26799-112">Exempel 1: Hämta alla data fabriker</span><span class="sxs-lookup"><span data-stu-id="26799-112">Example 1: Get all data factories</span></span>
```
PS C:\> Get-AzDataFactoryV2 -ResourceGroupName "ADF"

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

<span data-ttu-id="26799-113">Visar information om alla data faktorer i Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="26799-113">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="26799-114">Exempel 2: skaffa en specifik data fabrik</span><span class="sxs-lookup"><span data-stu-id="26799-114">Example 2: Get a specific data factory</span></span>
```
PS C:\> $DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
```

<span data-ttu-id="26799-115">Det här kommandot visar information om data fabriken med namnet WikiADF i prenumerationen för resurs gruppen med namnet ADF och sedan lagras den i $DataFactory variabel.</span><span class="sxs-lookup"><span data-stu-id="26799-115">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="26799-116">Ange parametern DataFactory i efterföljande cmdlets för att använda data fabriken som lagras i $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="26799-116">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="26799-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26799-117">PARAMETERS</span></span>

### <span data-ttu-id="26799-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26799-118">-DefaultProfile</span></span>
<span data-ttu-id="26799-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="26799-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26799-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="26799-120">-Name</span></span>
<span data-ttu-id="26799-121">Anger namnet på data fabriken för att få information.</span><span class="sxs-lookup"><span data-stu-id="26799-121">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26799-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26799-122">-ResourceGroupName</span></span>
<span data-ttu-id="26799-123">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="26799-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="26799-124">Denna cmdlet hämtar information om de data fabriker som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="26799-124">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26799-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26799-125">CommonParameters</span></span>
<span data-ttu-id="26799-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26799-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26799-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26799-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26799-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26799-128">INPUTS</span></span>

### <span data-ttu-id="26799-129">System. String</span><span class="sxs-lookup"><span data-stu-id="26799-129">System.String</span></span>

## <span data-ttu-id="26799-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26799-130">OUTPUTS</span></span>

### <span data-ttu-id="26799-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="26799-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="26799-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26799-132">NOTES</span></span>
<span data-ttu-id="26799-133">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="26799-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="26799-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26799-134">RELATED LINKS</span></span>

[<span data-ttu-id="26799-135">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="26799-135">Set-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="26799-136">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="26799-136">Remove-AzDataFactoryV2</span></span>]()


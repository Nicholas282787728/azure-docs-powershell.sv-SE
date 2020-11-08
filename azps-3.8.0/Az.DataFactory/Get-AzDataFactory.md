---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
ms.openlocfilehash: 11aaaa3bb17a35583655f231123b7f6e9dea9ab4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091828"
---
# <span data-ttu-id="da9e1-101">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="da9e1-101">Get-AzDataFactory</span></span>

## <span data-ttu-id="da9e1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da9e1-102">SYNOPSIS</span></span>
<span data-ttu-id="da9e1-103">Hämtar information om data fabriker.</span><span class="sxs-lookup"><span data-stu-id="da9e1-103">Gets information about Data Factories.</span></span>

## <span data-ttu-id="da9e1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da9e1-104">SYNTAX</span></span>

```
Get-AzDataFactory [[-Name] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da9e1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da9e1-105">DESCRIPTION</span></span>
<span data-ttu-id="da9e1-106">Cmdleten **Get-AzDataFactory** hämtar information om data fabrikerna i en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="da9e1-106">The **Get-AzDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="da9e1-107">Om du anger namnet på en data fabrik får denna cmdlet information om den data fabriken.</span><span class="sxs-lookup"><span data-stu-id="da9e1-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="da9e1-108">Om du inte anger ett namn hämtas den här cmdleten information om alla data fabrikerna i en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="da9e1-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="da9e1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da9e1-109">EXAMPLES</span></span>

### <span data-ttu-id="da9e1-110">Exempel 1: Hämta alla data fabriker</span><span class="sxs-lookup"><span data-stu-id="da9e1-110">Example 1: Get all data factories</span></span>
```
PS C:\>Get-AzDataFactory -ResourceGroupName "ADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration

DataFactoryName   : WikiADF2
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="da9e1-111">Det här kommandot visar information om alla data faktorer i Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="da9e1-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="da9e1-112">Exempel 2: skaffa en specifik data fabrik</span><span class="sxs-lookup"><span data-stu-id="da9e1-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="da9e1-113">Det här kommandot visar information om data fabriken med namnet WikiADF i prenumerationen för resurs gruppen med namnet ADF och sedan lagras den i $DataFactory variabel.</span><span class="sxs-lookup"><span data-stu-id="da9e1-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="da9e1-114">Ange parametern *DataFactory* i efterföljande cmdlets för att använda data fabriken som lagras i $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="da9e1-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="da9e1-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da9e1-115">PARAMETERS</span></span>

### <span data-ttu-id="da9e1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da9e1-116">-DefaultProfile</span></span>
<span data-ttu-id="da9e1-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="da9e1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da9e1-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="da9e1-118">-Name</span></span>
<span data-ttu-id="da9e1-119">Anger namnet på data fabriken för att få information.</span><span class="sxs-lookup"><span data-stu-id="da9e1-119">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da9e1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da9e1-120">-ResourceGroupName</span></span>
<span data-ttu-id="da9e1-121">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="da9e1-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="da9e1-122">Denna cmdlet hämtar information om data fabriker som tillhör gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="da9e1-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da9e1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da9e1-123">CommonParameters</span></span>
<span data-ttu-id="da9e1-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da9e1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da9e1-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da9e1-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da9e1-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da9e1-126">INPUTS</span></span>

### <span data-ttu-id="da9e1-127">System. String</span><span class="sxs-lookup"><span data-stu-id="da9e1-127">System.String</span></span>

## <span data-ttu-id="da9e1-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da9e1-128">OUTPUTS</span></span>

### <span data-ttu-id="da9e1-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="da9e1-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="da9e1-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da9e1-130">NOTES</span></span>
* <span data-ttu-id="da9e1-131">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="da9e1-131">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="da9e1-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da9e1-132">RELATED LINKS</span></span>

[<span data-ttu-id="da9e1-133">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="da9e1-133">New-AzDataFactory</span></span>](./New-AzDataFactory.md)

[<span data-ttu-id="da9e1-134">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="da9e1-134">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)



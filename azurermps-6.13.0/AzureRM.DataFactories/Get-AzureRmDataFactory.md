---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
ms.openlocfilehash: cfe19786e0d40915fc9cac67561b7e99b5dac38e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757899"
---
# <span data-ttu-id="ecd06-101">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="ecd06-101">Get-AzureRmDataFactory</span></span>

## <span data-ttu-id="ecd06-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ecd06-102">SYNOPSIS</span></span>
<span data-ttu-id="ecd06-103">Hämtar information om data fabriker.</span><span class="sxs-lookup"><span data-stu-id="ecd06-103">Gets information about Data Factories.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecd06-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ecd06-104">SYNTAX</span></span>

```
Get-AzureRmDataFactory [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecd06-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ecd06-105">DESCRIPTION</span></span>
<span data-ttu-id="ecd06-106">Cmdleten **Get-AzureRmDataFactory** hämtar information om data fabrikerna i en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ecd06-106">The **Get-AzureRmDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="ecd06-107">Om du anger namnet på en data fabrik får denna cmdlet information om den data fabriken.</span><span class="sxs-lookup"><span data-stu-id="ecd06-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="ecd06-108">Om du inte anger ett namn hämtas den här cmdleten information om alla data fabrikerna i en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ecd06-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="ecd06-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ecd06-109">EXAMPLES</span></span>

### <span data-ttu-id="ecd06-110">Exempel 1: Hämta alla data fabriker</span><span class="sxs-lookup"><span data-stu-id="ecd06-110">Example 1: Get all data factories</span></span>
```
PS C:\>Get-AzureRmDataFactory -ResourceGroupName "ADF"
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

<span data-ttu-id="ecd06-111">Det här kommandot visar information om alla data faktorer i Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="ecd06-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="ecd06-112">Exempel 2: skaffa en specifik data fabrik</span><span class="sxs-lookup"><span data-stu-id="ecd06-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="ecd06-113">Det här kommandot visar information om data fabriken med namnet WikiADF i prenumerationen för resurs gruppen med namnet ADF och sedan lagras den i $DataFactory variabel.</span><span class="sxs-lookup"><span data-stu-id="ecd06-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="ecd06-114">Ange parametern *DataFactory* i efterföljande cmdlets för att använda data fabriken som lagras i $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="ecd06-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="ecd06-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ecd06-115">PARAMETERS</span></span>

### <span data-ttu-id="ecd06-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecd06-116">-DefaultProfile</span></span>
<span data-ttu-id="ecd06-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ecd06-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecd06-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ecd06-118">-Name</span></span>
<span data-ttu-id="ecd06-119">Anger namnet på data fabriken för att få information.</span><span class="sxs-lookup"><span data-stu-id="ecd06-119">Specifies the name of the data factory about which to get information.</span></span>

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

### <span data-ttu-id="ecd06-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecd06-120">-ResourceGroupName</span></span>
<span data-ttu-id="ecd06-121">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="ecd06-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ecd06-122">Denna cmdlet hämtar information om data fabriker som tillhör gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="ecd06-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ecd06-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecd06-123">CommonParameters</span></span>
<span data-ttu-id="ecd06-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecd06-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecd06-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecd06-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecd06-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ecd06-126">INPUTS</span></span>

### <span data-ttu-id="ecd06-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ecd06-127">System.String</span></span>

## <span data-ttu-id="ecd06-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ecd06-128">OUTPUTS</span></span>

### <span data-ttu-id="ecd06-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ecd06-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="ecd06-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ecd06-130">NOTES</span></span>
* <span data-ttu-id="ecd06-131">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="ecd06-131">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ecd06-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ecd06-132">RELATED LINKS</span></span>

[<span data-ttu-id="ecd06-133">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="ecd06-133">New-AzureRmDataFactory</span></span>](./New-AzureRmDataFactory.md)

[<span data-ttu-id="ecd06-134">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="ecd06-134">Remove-AzureRmDataFactory</span></span>](./Remove-AzureRmDataFactory.md)



---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
ms.openlocfilehash: 2f0f4ea68de5071a860b55a464d339d65ff2882c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573486"
---
# <span data-ttu-id="10708-101">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="10708-101">Get-AzureRmDataFactory</span></span>

## <span data-ttu-id="10708-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10708-102">SYNOPSIS</span></span>
<span data-ttu-id="10708-103">Hämtar information om data fabriker.</span><span class="sxs-lookup"><span data-stu-id="10708-103">Gets information about Data Factories.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10708-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10708-104">SYNTAX</span></span>

```
Get-AzureRmDataFactory [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10708-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10708-105">DESCRIPTION</span></span>
<span data-ttu-id="10708-106">Cmdleten **Get-AzureRmDataFactory** hämtar information om data fabrikerna i en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="10708-106">The **Get-AzureRmDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="10708-107">Om du anger namnet på en data fabrik får denna cmdlet information om den data fabriken.</span><span class="sxs-lookup"><span data-stu-id="10708-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="10708-108">Om du inte anger ett namn hämtas den här cmdleten information om alla data fabrikerna i en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="10708-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="10708-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10708-109">EXAMPLES</span></span>

### <span data-ttu-id="10708-110">Exempel 1: Hämta alla data fabriker</span><span class="sxs-lookup"><span data-stu-id="10708-110">Example 1: Get all data factories</span></span>
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

<span data-ttu-id="10708-111">Det här kommandot visar information om alla data faktorer i Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="10708-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="10708-112">Exempel 2: skaffa en specifik data fabrik</span><span class="sxs-lookup"><span data-stu-id="10708-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="10708-113">Det här kommandot visar information om data fabriken med namnet WikiADF i prenumerationen för resurs gruppen med namnet ADF och sedan lagras den i $DataFactory variabel.</span><span class="sxs-lookup"><span data-stu-id="10708-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="10708-114">Ange parametern *DataFactory* i efterföljande cmdlets för att använda data fabriken som lagras i $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="10708-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="10708-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10708-115">PARAMETERS</span></span>

### <span data-ttu-id="10708-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10708-116">-DefaultProfile</span></span>
<span data-ttu-id="10708-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="10708-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10708-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="10708-118">-Name</span></span>
<span data-ttu-id="10708-119">Anger namnet på data fabriken för att få information.</span><span class="sxs-lookup"><span data-stu-id="10708-119">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10708-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10708-120">-ResourceGroupName</span></span>
<span data-ttu-id="10708-121">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="10708-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="10708-122">Denna cmdlet hämtar information om data fabriker som tillhör gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="10708-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="10708-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10708-123">CommonParameters</span></span>
<span data-ttu-id="10708-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10708-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10708-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10708-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10708-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10708-126">INPUTS</span></span>

### <span data-ttu-id="10708-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="10708-127">None</span></span>
<span data-ttu-id="10708-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="10708-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="10708-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10708-129">OUTPUTS</span></span>

### <span data-ttu-id="10708-130">System. Collections. Generic. list ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory, Microsoft. WindowsAzure. commands. Utilities, version = 0.8.2.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="10708-130">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span></span>

## <span data-ttu-id="10708-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10708-131">NOTES</span></span>
* <span data-ttu-id="10708-132">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="10708-132">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="10708-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10708-133">RELATED LINKS</span></span>

[<span data-ttu-id="10708-134">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="10708-134">New-AzureRmDataFactory</span></span>](./New-AzureRmDataFactory.md)

[<span data-ttu-id="10708-135">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="10708-135">Remove-AzureRmDataFactory</span></span>](./Remove-AzureRmDataFactory.md)



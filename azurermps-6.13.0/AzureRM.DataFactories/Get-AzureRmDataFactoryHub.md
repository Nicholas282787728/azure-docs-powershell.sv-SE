---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
ms.openlocfilehash: d1015a5f401b0cb91731bafe93ead02e2bf3068f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585027"
---
# <span data-ttu-id="a55f0-101">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="a55f0-101">Get-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="a55f0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a55f0-102">SYNOPSIS</span></span>
<span data-ttu-id="a55f0-103">Hämtar information om hubbarna i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a55f0-103">Gets information about hubs in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a55f0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a55f0-104">SYNTAX</span></span>

### <span data-ttu-id="a55f0-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="a55f0-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a55f0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a55f0-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a55f0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a55f0-107">DESCRIPTION</span></span>
<span data-ttu-id="a55f0-108">Cmdleten **Get-AzureRmDataFactoryHub** hämtar information om hubbarna i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a55f0-108">The **Get-AzureRmDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="a55f0-109">Om du anger namnet på en hubb får denna cmdlet information om det navet.</span><span class="sxs-lookup"><span data-stu-id="a55f0-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="a55f0-110">Om du inte anger ett namn får den här cmdleten information om alla hubbarna i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="a55f0-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="a55f0-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a55f0-111">EXAMPLES</span></span>

### <span data-ttu-id="a55f0-112">Exempel 1: Hämta alla data nav</span><span class="sxs-lookup"><span data-stu-id="a55f0-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="a55f0-113">Det här kommandot får alla data nav i Azure-gruppgruppen med namnet ADFResourceGroup och data fabriken med namnet ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="a55f0-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="a55f0-114">Exempel 2: skaffa ett specifikt data nav</span><span class="sxs-lookup"><span data-stu-id="a55f0-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="a55f0-115">Med det här kommandot får du information om navet som heter MyDataHub i Azure Resource Group med namnet ADFResourceGroup och data fabriken med namnet ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="a55f0-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="a55f0-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a55f0-116">PARAMETERS</span></span>

### <span data-ttu-id="a55f0-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a55f0-117">-DataFactory</span></span>
<span data-ttu-id="a55f0-118">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="a55f0-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="a55f0-119">Denna cmdlet får information om de nav i data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="a55f0-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a55f0-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a55f0-120">-DataFactoryName</span></span>
<span data-ttu-id="a55f0-121">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="a55f0-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a55f0-122">Denna cmdlet får information om de nav i data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="a55f0-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a55f0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a55f0-123">-DefaultProfile</span></span>
<span data-ttu-id="a55f0-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a55f0-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a55f0-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="a55f0-125">-Name</span></span>
<span data-ttu-id="a55f0-126">Anger namnet på navet där informationen ska visas.</span><span class="sxs-lookup"><span data-stu-id="a55f0-126">Specifies the name of the hub about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a55f0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a55f0-127">-ResourceGroupName</span></span>
<span data-ttu-id="a55f0-128">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="a55f0-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a55f0-129">Med den här cmdleten får du information om de nav som tillhör gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="a55f0-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a55f0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a55f0-130">CommonParameters</span></span>
<span data-ttu-id="a55f0-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a55f0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a55f0-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a55f0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a55f0-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a55f0-133">INPUTS</span></span>

### <span data-ttu-id="a55f0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a55f0-134">System.String</span></span>

### <span data-ttu-id="a55f0-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a55f0-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="a55f0-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a55f0-136">OUTPUTS</span></span>

### <span data-ttu-id="a55f0-137">Microsoft. Azure. commands. DataFactories. Models. PSHub</span><span class="sxs-lookup"><span data-stu-id="a55f0-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="a55f0-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a55f0-138">NOTES</span></span>
* <span data-ttu-id="a55f0-139">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="a55f0-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a55f0-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a55f0-140">RELATED LINKS</span></span>

[<span data-ttu-id="a55f0-141">New-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="a55f0-141">New-AzureRmDataFactoryHub</span></span>](./New-AzureRmDataFactoryHub.md)

[<span data-ttu-id="a55f0-142">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="a55f0-142">Remove-AzureRmDataFactoryHub</span></span>](./Remove-AzureRmDataFactoryHub.md)



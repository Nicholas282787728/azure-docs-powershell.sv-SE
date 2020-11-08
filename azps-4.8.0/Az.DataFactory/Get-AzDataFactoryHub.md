---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
ms.openlocfilehash: 292a288850371a834f938143cf2ec4380504091b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260258"
---
# <span data-ttu-id="534ce-101">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="534ce-101">Get-AzDataFactoryHub</span></span>

## <span data-ttu-id="534ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="534ce-102">SYNOPSIS</span></span>
<span data-ttu-id="534ce-103">Hämtar information om hubbarna i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="534ce-103">Gets information about hubs in Azure Data Factory.</span></span>

## <span data-ttu-id="534ce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="534ce-104">SYNTAX</span></span>

### <span data-ttu-id="534ce-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="534ce-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="534ce-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="534ce-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="534ce-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="534ce-107">DESCRIPTION</span></span>
<span data-ttu-id="534ce-108">Cmdleten **Get-AzDataFactoryHub** hämtar information om hubbarna i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="534ce-108">The **Get-AzDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="534ce-109">Om du anger namnet på en hubb får denna cmdlet information om det navet.</span><span class="sxs-lookup"><span data-stu-id="534ce-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="534ce-110">Om du inte anger ett namn får den här cmdleten information om alla hubbarna i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="534ce-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="534ce-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="534ce-111">EXAMPLES</span></span>

### <span data-ttu-id="534ce-112">Exempel 1: Hämta alla data nav</span><span class="sxs-lookup"><span data-stu-id="534ce-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="534ce-113">Det här kommandot får alla data nav i Azure-gruppgruppen med namnet ADFResourceGroup och data fabriken med namnet ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="534ce-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="534ce-114">Exempel 2: skaffa ett specifikt data nav</span><span class="sxs-lookup"><span data-stu-id="534ce-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="534ce-115">Med det här kommandot får du information om navet som heter MyDataHub i Azure Resource Group med namnet ADFResourceGroup och data fabriken med namnet ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="534ce-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="534ce-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="534ce-116">PARAMETERS</span></span>

### <span data-ttu-id="534ce-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="534ce-117">-DataFactory</span></span>
<span data-ttu-id="534ce-118">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="534ce-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="534ce-119">Denna cmdlet får information om de nav i data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="534ce-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="534ce-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="534ce-120">-DataFactoryName</span></span>
<span data-ttu-id="534ce-121">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="534ce-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="534ce-122">Denna cmdlet får information om de nav i data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="534ce-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="534ce-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="534ce-123">-DefaultProfile</span></span>
<span data-ttu-id="534ce-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="534ce-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="534ce-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="534ce-125">-Name</span></span>
<span data-ttu-id="534ce-126">Anger namnet på navet där informationen ska visas.</span><span class="sxs-lookup"><span data-stu-id="534ce-126">Specifies the name of the hub about which to get information.</span></span>

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

### <span data-ttu-id="534ce-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="534ce-127">-ResourceGroupName</span></span>
<span data-ttu-id="534ce-128">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="534ce-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="534ce-129">Med den här cmdleten får du information om de nav som tillhör gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="534ce-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="534ce-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="534ce-130">CommonParameters</span></span>
<span data-ttu-id="534ce-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="534ce-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="534ce-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="534ce-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="534ce-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="534ce-133">INPUTS</span></span>

### <span data-ttu-id="534ce-134">System. String</span><span class="sxs-lookup"><span data-stu-id="534ce-134">System.String</span></span>

### <span data-ttu-id="534ce-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="534ce-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="534ce-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="534ce-136">OUTPUTS</span></span>

### <span data-ttu-id="534ce-137">Microsoft. Azure. commands. DataFactories. Models. PSHub</span><span class="sxs-lookup"><span data-stu-id="534ce-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="534ce-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="534ce-138">NOTES</span></span>
* <span data-ttu-id="534ce-139">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="534ce-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="534ce-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="534ce-140">RELATED LINKS</span></span>

[<span data-ttu-id="534ce-141">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="534ce-141">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)

[<span data-ttu-id="534ce-142">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="534ce-142">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)



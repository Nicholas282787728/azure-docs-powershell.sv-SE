---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
ms.openlocfilehash: 12a18c62d3cc3412726df323bd48acd86ed7b1fd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927774"
---
# <span data-ttu-id="4b45f-101">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="4b45f-101">Remove-AzDataFactoryHub</span></span>

## <span data-ttu-id="4b45f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4b45f-102">SYNOPSIS</span></span>
<span data-ttu-id="4b45f-103">Tar bort ett nav från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="4b45f-103">Removes a hub from Azure Data Factory.</span></span>

## <span data-ttu-id="4b45f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4b45f-104">SYNTAX</span></span>

### <span data-ttu-id="4b45f-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="4b45f-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b45f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4b45f-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b45f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4b45f-107">DESCRIPTION</span></span>
<span data-ttu-id="4b45f-108">Cmdleten **Remove-AzDataFactoryHub** tar bort ett nav från Azure Data Factory i den angivna Azure-resursen och i den angivna data fabriken.</span><span class="sxs-lookup"><span data-stu-id="4b45f-108">The **Remove-AzDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="4b45f-109">Om du tar bort ett nav tas även alla länkade tjänster och rörledningar bort från navet.</span><span class="sxs-lookup"><span data-stu-id="4b45f-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="4b45f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4b45f-110">EXAMPLES</span></span>

### <span data-ttu-id="4b45f-111">Exempel 1: ta bort ett nav</span><span class="sxs-lookup"><span data-stu-id="4b45f-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="4b45f-112">Det här kommandot tar bort navet som heter ContosoDataHub från Azure Resource Group med namnet ADFResourceGroup och data fabriken med namnet ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="4b45f-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="4b45f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4b45f-113">PARAMETERS</span></span>

### <span data-ttu-id="4b45f-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4b45f-114">-DataFactory</span></span>
<span data-ttu-id="4b45f-115">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="4b45f-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="4b45f-116">Denna cmdlet tar bort ett nav från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="4b45f-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4b45f-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4b45f-117">-DataFactoryName</span></span>
<span data-ttu-id="4b45f-118">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="4b45f-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4b45f-119">Denna cmdlet tar bort ett nav från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="4b45f-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4b45f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b45f-120">-DefaultProfile</span></span>
<span data-ttu-id="4b45f-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4b45f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b45f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="4b45f-122">-Force</span></span>
<span data-ttu-id="4b45f-123">Anger att denna cmdlet tar bort ett nav utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="4b45f-123">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b45f-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="4b45f-124">-Name</span></span>
<span data-ttu-id="4b45f-125">Anger namnet på navet som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4b45f-125">Specifies the name of the hub to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b45f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b45f-126">-ResourceGroupName</span></span>
<span data-ttu-id="4b45f-127">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="4b45f-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4b45f-128">Denna cmdlet tar bort ett nav från gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="4b45f-128">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4b45f-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4b45f-129">-Confirm</span></span>
<span data-ttu-id="4b45f-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4b45f-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b45f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b45f-131">-WhatIf</span></span>
<span data-ttu-id="4b45f-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4b45f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b45f-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4b45f-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b45f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b45f-134">CommonParameters</span></span>
<span data-ttu-id="4b45f-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b45f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b45f-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b45f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b45f-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4b45f-137">INPUTS</span></span>

### <span data-ttu-id="4b45f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4b45f-138">System.String</span></span>

### <span data-ttu-id="4b45f-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4b45f-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="4b45f-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4b45f-140">OUTPUTS</span></span>

### <span data-ttu-id="4b45f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4b45f-141">System.Boolean</span></span>

## <span data-ttu-id="4b45f-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4b45f-142">NOTES</span></span>
* <span data-ttu-id="4b45f-143">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="4b45f-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4b45f-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4b45f-144">RELATED LINKS</span></span>

[<span data-ttu-id="4b45f-145">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="4b45f-145">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="4b45f-146">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="4b45f-146">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)


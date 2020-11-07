---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryHub.md
ms.openlocfilehash: 09e78957b3eef48731f2226a0737d0017c1e9b98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756209"
---
# <span data-ttu-id="335e1-101">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="335e1-101">Remove-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="335e1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="335e1-102">SYNOPSIS</span></span>
<span data-ttu-id="335e1-103">Tar bort ett nav från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="335e1-103">Removes a hub from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="335e1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="335e1-104">SYNTAX</span></span>

### <span data-ttu-id="335e1-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="335e1-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="335e1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="335e1-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="335e1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="335e1-107">DESCRIPTION</span></span>
<span data-ttu-id="335e1-108">Cmdleten **Remove-AzureRmDataFactoryHub** tar bort ett nav från Azure Data Factory i den angivna Azure-resursen och i den angivna data fabriken.</span><span class="sxs-lookup"><span data-stu-id="335e1-108">The **Remove-AzureRmDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="335e1-109">Om du tar bort ett nav tas även alla länkade tjänster och rörledningar bort från navet.</span><span class="sxs-lookup"><span data-stu-id="335e1-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="335e1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="335e1-110">EXAMPLES</span></span>

### <span data-ttu-id="335e1-111">Exempel 1: ta bort ett nav</span><span class="sxs-lookup"><span data-stu-id="335e1-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="335e1-112">Det här kommandot tar bort navet som heter ContosoDataHub från Azure Resource Group med namnet ADFResourceGroup och data fabriken med namnet ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="335e1-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="335e1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="335e1-113">PARAMETERS</span></span>

### <span data-ttu-id="335e1-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="335e1-114">-DataFactory</span></span>
<span data-ttu-id="335e1-115">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="335e1-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="335e1-116">Denna cmdlet tar bort ett nav från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="335e1-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="335e1-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="335e1-117">-DataFactoryName</span></span>
<span data-ttu-id="335e1-118">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="335e1-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="335e1-119">Denna cmdlet tar bort ett nav från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="335e1-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="335e1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="335e1-120">-DefaultProfile</span></span>
<span data-ttu-id="335e1-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="335e1-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="335e1-122">-Force</span><span class="sxs-lookup"><span data-stu-id="335e1-122">-Force</span></span>
<span data-ttu-id="335e1-123">Anger att denna cmdlet tar bort ett nav utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="335e1-123">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="335e1-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="335e1-124">-Name</span></span>
<span data-ttu-id="335e1-125">Anger namnet på navet som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="335e1-125">Specifies the name of the hub to remove.</span></span>

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

### <span data-ttu-id="335e1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="335e1-126">-ResourceGroupName</span></span>
<span data-ttu-id="335e1-127">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="335e1-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="335e1-128">Denna cmdlet tar bort ett nav från gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="335e1-128">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="335e1-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="335e1-129">-Confirm</span></span>
<span data-ttu-id="335e1-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="335e1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="335e1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="335e1-131">-WhatIf</span></span>
<span data-ttu-id="335e1-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="335e1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="335e1-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="335e1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="335e1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="335e1-134">CommonParameters</span></span>
<span data-ttu-id="335e1-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="335e1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="335e1-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="335e1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="335e1-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="335e1-137">INPUTS</span></span>

### <span data-ttu-id="335e1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="335e1-138">System.String</span></span>

### <span data-ttu-id="335e1-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="335e1-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="335e1-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="335e1-140">OUTPUTS</span></span>

### <span data-ttu-id="335e1-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="335e1-141">System.Boolean</span></span>

## <span data-ttu-id="335e1-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="335e1-142">NOTES</span></span>
* <span data-ttu-id="335e1-143">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="335e1-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="335e1-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="335e1-144">RELATED LINKS</span></span>

[<span data-ttu-id="335e1-145">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="335e1-145">Get-AzureRmDataFactoryHub</span></span>](./Get-AzureRmDataFactoryHub.md)

[<span data-ttu-id="335e1-146">New-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="335e1-146">New-AzureRmDataFactoryHub</span></span>](./New-AzureRmDataFactoryHub.md)



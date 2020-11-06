---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryHub.md
ms.openlocfilehash: 6788f2dea9cf46b888f729ab97640201f740e80d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579751"
---
# <span data-ttu-id="672b7-101">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="672b7-101">Remove-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="672b7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="672b7-102">SYNOPSIS</span></span>
<span data-ttu-id="672b7-103">Tar bort ett nav från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="672b7-103">Removes a hub from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="672b7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="672b7-104">SYNTAX</span></span>

### <span data-ttu-id="672b7-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="672b7-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="672b7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="672b7-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="672b7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="672b7-107">DESCRIPTION</span></span>
<span data-ttu-id="672b7-108">Cmdleten **Remove-AzureRmDataFactoryHub** tar bort ett nav från Azure Data Factory i den angivna Azure-resursen och i den angivna data fabriken.</span><span class="sxs-lookup"><span data-stu-id="672b7-108">The **Remove-AzureRmDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="672b7-109">Om du tar bort ett nav tas även alla länkade tjänster och rörledningar bort från navet.</span><span class="sxs-lookup"><span data-stu-id="672b7-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="672b7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="672b7-110">EXAMPLES</span></span>

### <span data-ttu-id="672b7-111">Exempel 1: ta bort ett nav</span><span class="sxs-lookup"><span data-stu-id="672b7-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="672b7-112">Det här kommandot tar bort navet som heter ContosoDataHub från Azure Resource Group med namnet ADFResourceGroup och data fabriken med namnet ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="672b7-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="672b7-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="672b7-113">PARAMETERS</span></span>

### <span data-ttu-id="672b7-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="672b7-114">-DataFactory</span></span>
<span data-ttu-id="672b7-115">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="672b7-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="672b7-116">Denna cmdlet tar bort ett nav från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="672b7-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="672b7-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="672b7-117">-DataFactoryName</span></span>
<span data-ttu-id="672b7-118">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="672b7-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="672b7-119">Denna cmdlet tar bort ett nav från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="672b7-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="672b7-120">-Force</span><span class="sxs-lookup"><span data-stu-id="672b7-120">-Force</span></span>
<span data-ttu-id="672b7-121">Anger att denna cmdlet tar bort ett nav utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="672b7-121">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="672b7-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="672b7-122">-Name</span></span>
<span data-ttu-id="672b7-123">Anger namnet på navet som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="672b7-123">Specifies the name of the hub to remove.</span></span>

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

### <span data-ttu-id="672b7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="672b7-124">-ResourceGroupName</span></span>
<span data-ttu-id="672b7-125">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="672b7-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="672b7-126">Denna cmdlet tar bort ett nav från gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="672b7-126">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="672b7-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="672b7-127">-Confirm</span></span>
<span data-ttu-id="672b7-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="672b7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="672b7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="672b7-129">-WhatIf</span></span>
<span data-ttu-id="672b7-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="672b7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="672b7-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="672b7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="672b7-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="672b7-132">-DefaultProfile</span></span>
<span data-ttu-id="672b7-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="672b7-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="672b7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="672b7-134">CommonParameters</span></span>
<span data-ttu-id="672b7-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="672b7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="672b7-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="672b7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="672b7-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="672b7-137">INPUTS</span></span>

## <span data-ttu-id="672b7-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="672b7-138">OUTPUTS</span></span>

### <span data-ttu-id="672b7-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="672b7-139">System.Boolean</span></span>

## <span data-ttu-id="672b7-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="672b7-140">NOTES</span></span>
* <span data-ttu-id="672b7-141">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="672b7-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="672b7-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="672b7-142">RELATED LINKS</span></span>

[<span data-ttu-id="672b7-143">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="672b7-143">Get-AzureRmDataFactoryHub</span></span>](./Get-AzureRmDataFactoryHub.md)

[<span data-ttu-id="672b7-144">New-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="672b7-144">New-AzureRmDataFactoryHub</span></span>](./New-AzureRmDataFactoryHub.md)



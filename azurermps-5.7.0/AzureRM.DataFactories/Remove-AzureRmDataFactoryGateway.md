---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryGateway.md
ms.openlocfilehash: b781207bae8b967acadf4a9ef3ae50c5ffc9cfef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577243"
---
# <span data-ttu-id="acd3d-101">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="acd3d-101">Remove-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="acd3d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="acd3d-102">SYNOPSIS</span></span>
<span data-ttu-id="acd3d-103">Tar bort en gateway från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="acd3d-103">Removes a gateway from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acd3d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="acd3d-104">SYNTAX</span></span>

### <span data-ttu-id="acd3d-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="acd3d-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="acd3d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="acd3d-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acd3d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="acd3d-107">DESCRIPTION</span></span>
<span data-ttu-id="acd3d-108">Cmdleten **Remove-AzureRmDataFactoryGateway** tar bort angiven Gateway från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="acd3d-108">The **Remove-AzureRmDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="acd3d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="acd3d-109">EXAMPLES</span></span>

### <span data-ttu-id="acd3d-110">Exempel 1: ta bort en gateway</span><span class="sxs-lookup"><span data-stu-id="acd3d-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzureRmDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="acd3d-111">Det här kommandot tar bort den gateway som heter ContosoGateway från data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="acd3d-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="acd3d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="acd3d-112">PARAMETERS</span></span>

### <span data-ttu-id="acd3d-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="acd3d-113">-DataFactory</span></span>
<span data-ttu-id="acd3d-114">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="acd3d-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="acd3d-115">Denna cmdlet tar bort en gateway från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="acd3d-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd3d-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="acd3d-116">-DataFactoryName</span></span>
<span data-ttu-id="acd3d-117">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="acd3d-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="acd3d-118">Denna cmdlet tar bort en gateway från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="acd3d-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd3d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acd3d-119">-DefaultProfile</span></span>
<span data-ttu-id="acd3d-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="acd3d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="acd3d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="acd3d-121">-Force</span></span>
<span data-ttu-id="acd3d-122">Anger att denna cmdlet tar bort en gateway utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="acd3d-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd3d-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="acd3d-123">-Name</span></span>
<span data-ttu-id="acd3d-124">Anger namnet på den gateway som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="acd3d-124">Specifies the name of the gateway to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd3d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acd3d-125">-ResourceGroupName</span></span>
<span data-ttu-id="acd3d-126">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="acd3d-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="acd3d-127">Denna cmdlet tar bort en gateway som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="acd3d-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd3d-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="acd3d-128">-Confirm</span></span>
<span data-ttu-id="acd3d-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="acd3d-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd3d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acd3d-130">-WhatIf</span></span>
<span data-ttu-id="acd3d-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="acd3d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acd3d-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="acd3d-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd3d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acd3d-133">CommonParameters</span></span>
<span data-ttu-id="acd3d-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acd3d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acd3d-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acd3d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acd3d-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="acd3d-136">INPUTS</span></span>

### <span data-ttu-id="acd3d-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="acd3d-137">None</span></span>
<span data-ttu-id="acd3d-138">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="acd3d-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="acd3d-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="acd3d-139">OUTPUTS</span></span>

### <span data-ttu-id="acd3d-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="acd3d-140">System.Boolean</span></span>

## <span data-ttu-id="acd3d-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="acd3d-141">NOTES</span></span>
* <span data-ttu-id="acd3d-142">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="acd3d-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="acd3d-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="acd3d-143">RELATED LINKS</span></span>

[<span data-ttu-id="acd3d-144">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="acd3d-144">Get-AzureRmDataFactoryGateway</span></span>](./Get-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="acd3d-145">New-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="acd3d-145">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="acd3d-146">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="acd3d-146">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)



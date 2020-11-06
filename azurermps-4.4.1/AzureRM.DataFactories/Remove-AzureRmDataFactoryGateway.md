---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryGateway.md
ms.openlocfilehash: d9ae03325afbfe81c47847cb27df75973221667b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578408"
---
# <span data-ttu-id="86df0-101">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="86df0-101">Remove-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="86df0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="86df0-102">SYNOPSIS</span></span>
<span data-ttu-id="86df0-103">Tar bort en gateway från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="86df0-103">Removes a gateway from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86df0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="86df0-104">SYNTAX</span></span>

### <span data-ttu-id="86df0-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="86df0-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="86df0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="86df0-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86df0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="86df0-107">DESCRIPTION</span></span>
<span data-ttu-id="86df0-108">Cmdleten **Remove-AzureRmDataFactoryGateway** tar bort angiven Gateway från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="86df0-108">The **Remove-AzureRmDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="86df0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="86df0-109">EXAMPLES</span></span>

### <span data-ttu-id="86df0-110">Exempel 1: ta bort en gateway</span><span class="sxs-lookup"><span data-stu-id="86df0-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzureRmDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="86df0-111">Det här kommandot tar bort den gateway som heter ContosoGateway från data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="86df0-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="86df0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="86df0-112">PARAMETERS</span></span>

### <span data-ttu-id="86df0-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="86df0-113">-DataFactory</span></span>
<span data-ttu-id="86df0-114">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="86df0-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="86df0-115">Denna cmdlet tar bort en gateway från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="86df0-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="86df0-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="86df0-116">-DataFactoryName</span></span>
<span data-ttu-id="86df0-117">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="86df0-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="86df0-118">Denna cmdlet tar bort en gateway från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="86df0-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="86df0-119">-Force</span><span class="sxs-lookup"><span data-stu-id="86df0-119">-Force</span></span>
<span data-ttu-id="86df0-120">Anger att denna cmdlet tar bort en gateway utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="86df0-120">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="86df0-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="86df0-121">-Name</span></span>
<span data-ttu-id="86df0-122">Anger namnet på den gateway som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="86df0-122">Specifies the name of the gateway to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86df0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86df0-123">-ResourceGroupName</span></span>
<span data-ttu-id="86df0-124">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="86df0-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="86df0-125">Denna cmdlet tar bort en gateway som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="86df0-125">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="86df0-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="86df0-126">-Confirm</span></span>
<span data-ttu-id="86df0-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="86df0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86df0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86df0-128">-WhatIf</span></span>
<span data-ttu-id="86df0-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="86df0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86df0-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="86df0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86df0-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86df0-131">-DefaultProfile</span></span>
<span data-ttu-id="86df0-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="86df0-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86df0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86df0-133">CommonParameters</span></span>
<span data-ttu-id="86df0-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86df0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86df0-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86df0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86df0-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="86df0-136">INPUTS</span></span>

## <span data-ttu-id="86df0-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="86df0-137">OUTPUTS</span></span>

### <span data-ttu-id="86df0-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="86df0-138">System.Boolean</span></span>

## <span data-ttu-id="86df0-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="86df0-139">NOTES</span></span>
* <span data-ttu-id="86df0-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="86df0-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="86df0-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="86df0-141">RELATED LINKS</span></span>

[<span data-ttu-id="86df0-142">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="86df0-142">Get-AzureRmDataFactoryGateway</span></span>](./Get-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="86df0-143">New-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="86df0-143">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="86df0-144">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="86df0-144">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)



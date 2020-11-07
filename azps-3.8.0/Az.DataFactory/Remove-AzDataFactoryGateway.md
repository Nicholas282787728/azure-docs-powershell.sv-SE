---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
ms.openlocfilehash: 6831395c4f3d63dc056729b22573a16d863013e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927773"
---
# <span data-ttu-id="017df-101">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="017df-101">Remove-AzDataFactoryGateway</span></span>

## <span data-ttu-id="017df-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="017df-102">SYNOPSIS</span></span>
<span data-ttu-id="017df-103">Tar bort en gateway från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="017df-103">Removes a gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="017df-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="017df-104">SYNTAX</span></span>

### <span data-ttu-id="017df-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="017df-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="017df-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="017df-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="017df-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="017df-107">DESCRIPTION</span></span>
<span data-ttu-id="017df-108">Cmdleten **Remove-AzDataFactoryGateway** tar bort angiven Gateway från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="017df-108">The **Remove-AzDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="017df-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="017df-109">EXAMPLES</span></span>

### <span data-ttu-id="017df-110">Exempel 1: ta bort en gateway</span><span class="sxs-lookup"><span data-stu-id="017df-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="017df-111">Det här kommandot tar bort den gateway som heter ContosoGateway från data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="017df-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="017df-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="017df-112">PARAMETERS</span></span>

### <span data-ttu-id="017df-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="017df-113">-DataFactory</span></span>
<span data-ttu-id="017df-114">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="017df-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="017df-115">Denna cmdlet tar bort en gateway från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="017df-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="017df-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="017df-116">-DataFactoryName</span></span>
<span data-ttu-id="017df-117">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="017df-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="017df-118">Denna cmdlet tar bort en gateway från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="017df-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="017df-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="017df-119">-DefaultProfile</span></span>
<span data-ttu-id="017df-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="017df-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="017df-121">-Force</span><span class="sxs-lookup"><span data-stu-id="017df-121">-Force</span></span>
<span data-ttu-id="017df-122">Anger att denna cmdlet tar bort en gateway utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="017df-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="017df-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="017df-123">-Name</span></span>
<span data-ttu-id="017df-124">Anger namnet på den gateway som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="017df-124">Specifies the name of the gateway to remove.</span></span>

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

### <span data-ttu-id="017df-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="017df-125">-ResourceGroupName</span></span>
<span data-ttu-id="017df-126">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="017df-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="017df-127">Denna cmdlet tar bort en gateway som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="017df-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="017df-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="017df-128">-Confirm</span></span>
<span data-ttu-id="017df-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="017df-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="017df-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="017df-130">-WhatIf</span></span>
<span data-ttu-id="017df-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="017df-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="017df-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="017df-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="017df-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="017df-133">CommonParameters</span></span>
<span data-ttu-id="017df-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="017df-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="017df-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="017df-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="017df-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="017df-136">INPUTS</span></span>

### <span data-ttu-id="017df-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="017df-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="017df-138">System. String</span><span class="sxs-lookup"><span data-stu-id="017df-138">System.String</span></span>

## <span data-ttu-id="017df-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="017df-139">OUTPUTS</span></span>

### <span data-ttu-id="017df-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="017df-140">System.Boolean</span></span>

## <span data-ttu-id="017df-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="017df-141">NOTES</span></span>
* <span data-ttu-id="017df-142">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="017df-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="017df-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="017df-143">RELATED LINKS</span></span>

[<span data-ttu-id="017df-144">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="017df-144">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="017df-145">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="017df-145">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="017df-146">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="017df-146">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)



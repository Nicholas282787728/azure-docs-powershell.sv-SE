---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
ms.openlocfilehash: 36c22a432d4e281600a1b718c1ac58a851fb7069
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927777"
---
# <span data-ttu-id="13f89-101">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="13f89-101">Remove-AzDataFactory</span></span>

## <span data-ttu-id="13f89-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13f89-102">SYNOPSIS</span></span>
<span data-ttu-id="13f89-103">Tar bort en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="13f89-103">Removes a data factory.</span></span>

## <span data-ttu-id="13f89-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13f89-104">SYNTAX</span></span>

### <span data-ttu-id="13f89-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="13f89-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13f89-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="13f89-106">ByFactoryObject</span></span>
```
Remove-AzDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13f89-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13f89-107">DESCRIPTION</span></span>
<span data-ttu-id="13f89-108">Cmdleten **Remove-AzDataFactory** tar bort en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="13f89-108">The **Remove-AzDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="13f89-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13f89-109">EXAMPLES</span></span>

### <span data-ttu-id="13f89-110">Exempel 1: ta bort en data fabrik</span><span class="sxs-lookup"><span data-stu-id="13f89-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="13f89-111">Det här kommandot tar bort data fabriken med namnet WikiADF från resurs gruppen med namnet ADF.</span><span class="sxs-lookup"><span data-stu-id="13f89-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="13f89-112">Det här kommandot returnerar ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="13f89-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="13f89-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13f89-113">PARAMETERS</span></span>

### <span data-ttu-id="13f89-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="13f89-114">-DataFactory</span></span>
<span data-ttu-id="13f89-115">Anger det **PSDataFactory** -objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="13f89-115">Specifies the **PSDataFactory** object to remove.</span></span>

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

### <span data-ttu-id="13f89-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13f89-116">-DefaultProfile</span></span>
<span data-ttu-id="13f89-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="13f89-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13f89-118">-Force</span><span class="sxs-lookup"><span data-stu-id="13f89-118">-Force</span></span>
<span data-ttu-id="13f89-119">Anger att denna cmdlet tar bort en data fabrik utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="13f89-119">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="13f89-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="13f89-120">-Name</span></span>
<span data-ttu-id="13f89-121">Anger namnet på data fabriken som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="13f89-121">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13f89-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13f89-122">-ResourceGroupName</span></span>
<span data-ttu-id="13f89-123">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="13f89-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="13f89-124">Denna cmdlet tar bort en data fabrik från den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="13f89-124">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="13f89-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="13f89-125">-Confirm</span></span>
<span data-ttu-id="13f89-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="13f89-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13f89-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13f89-127">-WhatIf</span></span>
<span data-ttu-id="13f89-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="13f89-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13f89-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="13f89-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13f89-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13f89-130">CommonParameters</span></span>
<span data-ttu-id="13f89-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13f89-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13f89-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13f89-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13f89-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13f89-133">INPUTS</span></span>

### <span data-ttu-id="13f89-134">System. String</span><span class="sxs-lookup"><span data-stu-id="13f89-134">System.String</span></span>

### <span data-ttu-id="13f89-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="13f89-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="13f89-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13f89-136">OUTPUTS</span></span>

### <span data-ttu-id="13f89-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="13f89-137">System.Void</span></span>

## <span data-ttu-id="13f89-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13f89-138">NOTES</span></span>
* <span data-ttu-id="13f89-139">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="13f89-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="13f89-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13f89-140">RELATED LINKS</span></span>

[<span data-ttu-id="13f89-141">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="13f89-141">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="13f89-142">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="13f89-142">New-AzDataFactory</span></span>](./New-AzDataFactory.md)



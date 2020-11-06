---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
ms.openlocfilehash: 212e0c2ee4863c6d18873a717ff25f6940c34a15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575697"
---
# <span data-ttu-id="d11f6-101">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="d11f6-101">Remove-AzureRmDataFactory</span></span>

## <span data-ttu-id="d11f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d11f6-102">SYNOPSIS</span></span>
<span data-ttu-id="d11f6-103">Tar bort en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="d11f6-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d11f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d11f6-104">SYNTAX</span></span>

### <span data-ttu-id="d11f6-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="d11f6-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d11f6-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d11f6-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d11f6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d11f6-107">DESCRIPTION</span></span>
<span data-ttu-id="d11f6-108">Cmdleten **Remove-AzureRmDataFactory** tar bort en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="d11f6-108">The **Remove-AzureRmDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="d11f6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d11f6-109">EXAMPLES</span></span>

### <span data-ttu-id="d11f6-110">Exempel 1: ta bort en data fabrik</span><span class="sxs-lookup"><span data-stu-id="d11f6-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzureRmDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="d11f6-111">Det här kommandot tar bort data fabriken med namnet WikiADF från resurs gruppen med namnet ADF.</span><span class="sxs-lookup"><span data-stu-id="d11f6-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="d11f6-112">Det här kommandot returnerar ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="d11f6-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="d11f6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d11f6-113">PARAMETERS</span></span>

### <span data-ttu-id="d11f6-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d11f6-114">-DataFactory</span></span>
<span data-ttu-id="d11f6-115">Anger det **PSDataFactory** -objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d11f6-115">Specifies the **PSDataFactory** object to remove.</span></span>

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

### <span data-ttu-id="d11f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d11f6-116">-DefaultProfile</span></span>
<span data-ttu-id="d11f6-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d11f6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d11f6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d11f6-118">-Force</span></span>
<span data-ttu-id="d11f6-119">Anger att denna cmdlet tar bort en data fabrik utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="d11f6-119">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="d11f6-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="d11f6-120">-Name</span></span>
<span data-ttu-id="d11f6-121">Anger namnet på data fabriken som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d11f6-121">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d11f6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d11f6-122">-ResourceGroupName</span></span>
<span data-ttu-id="d11f6-123">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="d11f6-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d11f6-124">Denna cmdlet tar bort en data fabrik från den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="d11f6-124">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d11f6-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d11f6-125">-Confirm</span></span>
<span data-ttu-id="d11f6-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d11f6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d11f6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d11f6-127">-WhatIf</span></span>
<span data-ttu-id="d11f6-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d11f6-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d11f6-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d11f6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d11f6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d11f6-130">CommonParameters</span></span>
<span data-ttu-id="d11f6-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d11f6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d11f6-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d11f6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d11f6-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d11f6-133">INPUTS</span></span>

### <span data-ttu-id="d11f6-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="d11f6-134">None</span></span>
<span data-ttu-id="d11f6-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d11f6-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d11f6-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d11f6-136">OUTPUTS</span></span>

### <span data-ttu-id="d11f6-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d11f6-137">System.Boolean</span></span>

## <span data-ttu-id="d11f6-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d11f6-138">NOTES</span></span>
* <span data-ttu-id="d11f6-139">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="d11f6-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d11f6-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d11f6-140">RELATED LINKS</span></span>

[<span data-ttu-id="d11f6-141">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="d11f6-141">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="d11f6-142">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="d11f6-142">New-AzureRmDataFactory</span></span>](./New-AzureRmDataFactory.md)



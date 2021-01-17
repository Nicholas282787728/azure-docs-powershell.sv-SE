---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetAppfilesvolumepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
ms.openlocfilehash: 30d525ebcb7d80a24e11080ee265eb509f575ff6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422496"
---
# <span data-ttu-id="5fd02-101">Set-AzNetAppFilesVolumePool</span><span class="sxs-lookup"><span data-stu-id="5fd02-101">Set-AzNetAppFilesVolumePool</span></span>

## <span data-ttu-id="5fd02-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5fd02-102">SYNOPSIS</span></span>
<span data-ttu-id="5fd02-103">Byta pool för en Azure NetApp-volym (ANF).</span><span class="sxs-lookup"><span data-stu-id="5fd02-103">Change pool for an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="5fd02-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5fd02-104">SYNTAX</span></span>

### <span data-ttu-id="5fd02-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5fd02-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-NewPoolResourceId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fd02-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fd02-106">ByParentObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -Name <String> -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fd02-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fd02-107">ByResourceIdParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fd02-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fd02-108">ByObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fd02-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5fd02-109">DESCRIPTION</span></span>
<span data-ttu-id="5fd02-110">Cmdleten **set-AzNetAppFilesVolumePool** ändrar poolen för en ANF-volym.</span><span class="sxs-lookup"><span data-stu-id="5fd02-110">The **Set-AzNetAppFilesVolumePool** cmdlet changes the pool of an ANF volume.</span></span>

## <span data-ttu-id="5fd02-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5fd02-111">EXAMPLES</span></span>

### <span data-ttu-id="5fd02-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5fd02-112">Example 1</span></span>
```powershell
PS C:\>Set-AzNetAppFilesVolumePool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -NewPoolResourceId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="5fd02-113">Då ändras poolens adresspool till en med ID: t för 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span><span class="sxs-lookup"><span data-stu-id="5fd02-113">This changes the pool for the volume MyVolume to one with the Id of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="5fd02-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5fd02-114">PARAMETERS</span></span>

### <span data-ttu-id="5fd02-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5fd02-115">-AccountName</span></span>
<span data-ttu-id="5fd02-116">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="5fd02-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd02-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fd02-117">-DefaultProfile</span></span>
<span data-ttu-id="5fd02-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5fd02-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fd02-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fd02-119">-InputObject</span></span>
<span data-ttu-id="5fd02-120">Volume-objekt som ska flyttas</span><span class="sxs-lookup"><span data-stu-id="5fd02-120">The volume object to move</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd02-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="5fd02-121">-Name</span></span>
<span data-ttu-id="5fd02-122">Namnet på ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="5fd02-122">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd02-123">-NewPoolResourceId</span><span class="sxs-lookup"><span data-stu-id="5fd02-123">-NewPoolResourceId</span></span>
<span data-ttu-id="5fd02-124">ResourceId för kapacitets gruppen att flytta till.</span><span class="sxs-lookup"><span data-stu-id="5fd02-124">ResourceId of the capacity pool to move to.</span></span>
<span data-ttu-id="5fd02-125">UUID v4 som används för att identifiera poolen</span><span class="sxs-lookup"><span data-stu-id="5fd02-125">UUID v4 used to identify the pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd02-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="5fd02-126">-PoolName</span></span>
<span data-ttu-id="5fd02-127">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="5fd02-127">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd02-128">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="5fd02-128">-PoolObject</span></span>
<span data-ttu-id="5fd02-129">Det pool-objekt som innehåller volymen</span><span class="sxs-lookup"><span data-stu-id="5fd02-129">The pool object containing the volume</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd02-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fd02-130">-ResourceGroupName</span></span>
<span data-ttu-id="5fd02-131">ANF-volymens resurs grupp</span><span class="sxs-lookup"><span data-stu-id="5fd02-131">The resource group of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd02-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fd02-132">-ResourceId</span></span>
<span data-ttu-id="5fd02-133">Resurs-ID för ANF volym</span><span class="sxs-lookup"><span data-stu-id="5fd02-133">The resource id of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd02-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5fd02-134">-Confirm</span></span>
<span data-ttu-id="5fd02-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5fd02-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd02-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fd02-136">-WhatIf</span></span>
<span data-ttu-id="5fd02-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5fd02-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fd02-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5fd02-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd02-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fd02-139">CommonParameters</span></span>
<span data-ttu-id="5fd02-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fd02-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fd02-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5fd02-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fd02-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5fd02-142">INPUTS</span></span>

### <span data-ttu-id="5fd02-143">System. String</span><span class="sxs-lookup"><span data-stu-id="5fd02-143">System.String</span></span>

### <span data-ttu-id="5fd02-144">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="5fd02-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="5fd02-145">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="5fd02-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="5fd02-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5fd02-146">OUTPUTS</span></span>

### <span data-ttu-id="5fd02-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5fd02-147">System.Boolean</span></span>

## <span data-ttu-id="5fd02-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5fd02-148">NOTES</span></span>

## <span data-ttu-id="5fd02-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5fd02-149">RELATED LINKS</span></span>

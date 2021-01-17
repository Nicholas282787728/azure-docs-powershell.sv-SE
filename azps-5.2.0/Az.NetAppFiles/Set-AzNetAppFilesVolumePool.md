---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetAppfilesvolumepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
ms.openlocfilehash: 30d525ebcb7d80a24e11080ee265eb509f575ff6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418056"
---
# <span data-ttu-id="8c0ca-101">Set-AzNetAppFilesVolumePool</span><span class="sxs-lookup"><span data-stu-id="8c0ca-101">Set-AzNetAppFilesVolumePool</span></span>

## <span data-ttu-id="8c0ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8c0ca-102">SYNOPSIS</span></span>
<span data-ttu-id="8c0ca-103">Byta pool för en Azure NetApp-volym (ANF).</span><span class="sxs-lookup"><span data-stu-id="8c0ca-103">Change pool for an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="8c0ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8c0ca-104">SYNTAX</span></span>

### <span data-ttu-id="8c0ca-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8c0ca-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-NewPoolResourceId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c0ca-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c0ca-106">ByParentObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -Name <String> -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c0ca-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c0ca-107">ByResourceIdParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c0ca-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c0ca-108">ByObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c0ca-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8c0ca-109">DESCRIPTION</span></span>
<span data-ttu-id="8c0ca-110">Cmdleten **set-AzNetAppFilesVolumePool** ändrar poolen för en ANF-volym.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-110">The **Set-AzNetAppFilesVolumePool** cmdlet changes the pool of an ANF volume.</span></span>

## <span data-ttu-id="8c0ca-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8c0ca-111">EXAMPLES</span></span>

### <span data-ttu-id="8c0ca-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8c0ca-112">Example 1</span></span>
```powershell
PS C:\>Set-AzNetAppFilesVolumePool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -NewPoolResourceId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="8c0ca-113">Då ändras poolens adresspool till en med ID: t för 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span><span class="sxs-lookup"><span data-stu-id="8c0ca-113">This changes the pool for the volume MyVolume to one with the Id of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="8c0ca-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8c0ca-114">PARAMETERS</span></span>

### <span data-ttu-id="8c0ca-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8c0ca-115">-AccountName</span></span>
<span data-ttu-id="8c0ca-116">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="8c0ca-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="8c0ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c0ca-117">-DefaultProfile</span></span>
<span data-ttu-id="8c0ca-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c0ca-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c0ca-119">-InputObject</span></span>
<span data-ttu-id="8c0ca-120">Volume-objekt som ska flyttas</span><span class="sxs-lookup"><span data-stu-id="8c0ca-120">The volume object to move</span></span>

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

### <span data-ttu-id="8c0ca-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="8c0ca-121">-Name</span></span>
<span data-ttu-id="8c0ca-122">Namnet på ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="8c0ca-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="8c0ca-123">-NewPoolResourceId</span><span class="sxs-lookup"><span data-stu-id="8c0ca-123">-NewPoolResourceId</span></span>
<span data-ttu-id="8c0ca-124">ResourceId för kapacitets gruppen att flytta till.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-124">ResourceId of the capacity pool to move to.</span></span>
<span data-ttu-id="8c0ca-125">UUID v4 som används för att identifiera poolen</span><span class="sxs-lookup"><span data-stu-id="8c0ca-125">UUID v4 used to identify the pool</span></span>

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

### <span data-ttu-id="8c0ca-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="8c0ca-126">-PoolName</span></span>
<span data-ttu-id="8c0ca-127">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="8c0ca-127">The name of the ANF pool</span></span>

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

### <span data-ttu-id="8c0ca-128">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="8c0ca-128">-PoolObject</span></span>
<span data-ttu-id="8c0ca-129">Det pool-objekt som innehåller volymen</span><span class="sxs-lookup"><span data-stu-id="8c0ca-129">The pool object containing the volume</span></span>

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

### <span data-ttu-id="8c0ca-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c0ca-130">-ResourceGroupName</span></span>
<span data-ttu-id="8c0ca-131">ANF-volymens resurs grupp</span><span class="sxs-lookup"><span data-stu-id="8c0ca-131">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="8c0ca-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c0ca-132">-ResourceId</span></span>
<span data-ttu-id="8c0ca-133">Resurs-ID för ANF volym</span><span class="sxs-lookup"><span data-stu-id="8c0ca-133">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="8c0ca-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8c0ca-134">-Confirm</span></span>
<span data-ttu-id="8c0ca-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c0ca-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c0ca-136">-WhatIf</span></span>
<span data-ttu-id="8c0ca-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c0ca-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c0ca-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c0ca-139">CommonParameters</span></span>
<span data-ttu-id="8c0ca-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c0ca-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c0ca-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c0ca-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8c0ca-142">INPUTS</span></span>

### <span data-ttu-id="8c0ca-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8c0ca-143">System.String</span></span>

### <span data-ttu-id="8c0ca-144">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="8c0ca-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="8c0ca-145">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="8c0ca-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="8c0ca-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8c0ca-146">OUTPUTS</span></span>

### <span data-ttu-id="8c0ca-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8c0ca-147">System.Boolean</span></span>

## <span data-ttu-id="8c0ca-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8c0ca-148">NOTES</span></span>

## <span data-ttu-id="8c0ca-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8c0ca-149">RELATED LINKS</span></span>

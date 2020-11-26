---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 1d28420e9457826f7c851eb0d3013f36de9edbc2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273248"
---
# <span data-ttu-id="789ea-101">Remove-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="789ea-101">Remove-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="789ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="789ea-102">SYNOPSIS</span></span>
<span data-ttu-id="789ea-103">Tar bort en Azure NetApp-fil (ANF).</span><span class="sxs-lookup"><span data-stu-id="789ea-103">Deletes an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="789ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="789ea-104">SYNTAX</span></span>

### <span data-ttu-id="789ea-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="789ea-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="789ea-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="789ea-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="789ea-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="789ea-107">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="789ea-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="789ea-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -InputObject <PSNetAppFilesSnapshot> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="789ea-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="789ea-109">DESCRIPTION</span></span>
<span data-ttu-id="789ea-110">Cmdleten **Remove-AzNetAppFilesSnapshot** tar bort en ANF-stillbild.</span><span class="sxs-lookup"><span data-stu-id="789ea-110">The **Remove-AzNetAppFilesSnapshot** cmdlet deletes an ANF snapshot.</span></span>

## <span data-ttu-id="789ea-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="789ea-111">EXAMPLES</span></span>

### <span data-ttu-id="789ea-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="789ea-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"
```

<span data-ttu-id="789ea-113">Det här kommandot tar bort ANF Snapshot "MyAnfSnapshot".</span><span class="sxs-lookup"><span data-stu-id="789ea-113">This command deletes the ANF snapshot "MyAnfSnapshot".</span></span>

## <span data-ttu-id="789ea-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="789ea-114">PARAMETERS</span></span>

### <span data-ttu-id="789ea-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="789ea-115">-AccountName</span></span>
<span data-ttu-id="789ea-116">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="789ea-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="789ea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="789ea-117">-DefaultProfile</span></span>
<span data-ttu-id="789ea-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="789ea-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="789ea-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="789ea-119">-InputObject</span></span>
<span data-ttu-id="789ea-120">Det SnapShot-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="789ea-120">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="789ea-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="789ea-121">-Name</span></span>
<span data-ttu-id="789ea-122">Namn på ANF ögonblicks bild</span><span class="sxs-lookup"><span data-stu-id="789ea-122">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="789ea-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="789ea-123">-PassThru</span></span>
<span data-ttu-id="789ea-124">Returnera om den angivna volymen har tagits bort</span><span class="sxs-lookup"><span data-stu-id="789ea-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="789ea-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="789ea-125">-PoolName</span></span>
<span data-ttu-id="789ea-126">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="789ea-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="789ea-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="789ea-127">-ResourceGroupName</span></span>
<span data-ttu-id="789ea-128">ANF ögonblicks bild</span><span class="sxs-lookup"><span data-stu-id="789ea-128">The resource group of the ANF snapshot</span></span>

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

### <span data-ttu-id="789ea-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="789ea-129">-ResourceId</span></span>
<span data-ttu-id="789ea-130">Resurs-ID för ANF ögonblicks bild</span><span class="sxs-lookup"><span data-stu-id="789ea-130">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="789ea-131">-Volym namn</span><span class="sxs-lookup"><span data-stu-id="789ea-131">-VolumeName</span></span>
<span data-ttu-id="789ea-132">Namnet på ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="789ea-132">The name of the ANF volume</span></span>

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

### <span data-ttu-id="789ea-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="789ea-133">-VolumeObject</span></span>
<span data-ttu-id="789ea-134">Volume-objektet som innehåller den ögonblicks bild som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="789ea-134">The volume object containing the snapshot to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="789ea-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="789ea-135">-Confirm</span></span>
<span data-ttu-id="789ea-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="789ea-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="789ea-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="789ea-137">-WhatIf</span></span>
<span data-ttu-id="789ea-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="789ea-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="789ea-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="789ea-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="789ea-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="789ea-140">CommonParameters</span></span>
<span data-ttu-id="789ea-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="789ea-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="789ea-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="789ea-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="789ea-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="789ea-143">INPUTS</span></span>

### <span data-ttu-id="789ea-144">System. String</span><span class="sxs-lookup"><span data-stu-id="789ea-144">System.String</span></span>

### <span data-ttu-id="789ea-145">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="789ea-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="789ea-146">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="789ea-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="789ea-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="789ea-147">OUTPUTS</span></span>

### <span data-ttu-id="789ea-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="789ea-148">System.Boolean</span></span>

## <span data-ttu-id="789ea-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="789ea-149">NOTES</span></span>

## <span data-ttu-id="789ea-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="789ea-150">RELATED LINKS</span></span>
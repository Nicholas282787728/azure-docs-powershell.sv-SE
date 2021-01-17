---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: 9400efa61a98b6eb80b975d4999e03eb872e3b28
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411408"
---
# <span data-ttu-id="3ccfd-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="3ccfd-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="3ccfd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ccfd-102">SYNOPSIS</span></span>
<span data-ttu-id="3ccfd-103">Tar bort en Azure NetApp-fil (ANF).</span><span class="sxs-lookup"><span data-stu-id="3ccfd-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="3ccfd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ccfd-104">SYNTAX</span></span>

### <span data-ttu-id="3ccfd-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3ccfd-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ccfd-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ccfd-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ccfd-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ccfd-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ccfd-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ccfd-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ccfd-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ccfd-109">DESCRIPTION</span></span>
<span data-ttu-id="3ccfd-110">Cmdleten **Remove-AzNetAppFilesVolume** tar bort en ANF volym.</span><span class="sxs-lookup"><span data-stu-id="3ccfd-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="3ccfd-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ccfd-111">EXAMPLES</span></span>

### <span data-ttu-id="3ccfd-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3ccfd-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="3ccfd-113">Det här kommandot tar bort ANF volymen "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="3ccfd-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="3ccfd-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ccfd-114">PARAMETERS</span></span>

### <span data-ttu-id="3ccfd-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3ccfd-115">-AccountName</span></span>
<span data-ttu-id="3ccfd-116">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="3ccfd-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="3ccfd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ccfd-117">-DefaultProfile</span></span>
<span data-ttu-id="3ccfd-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3ccfd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ccfd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ccfd-119">-InputObject</span></span>
<span data-ttu-id="3ccfd-120">Volume-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="3ccfd-120">The volume object to remove</span></span>

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

### <span data-ttu-id="3ccfd-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="3ccfd-121">-Name</span></span>
<span data-ttu-id="3ccfd-122">Namnet på ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="3ccfd-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="3ccfd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ccfd-123">-PassThru</span></span>
<span data-ttu-id="3ccfd-124">Returnera om den angivna volymen har tagits bort</span><span class="sxs-lookup"><span data-stu-id="3ccfd-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="3ccfd-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="3ccfd-125">-PoolName</span></span>
<span data-ttu-id="3ccfd-126">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="3ccfd-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="3ccfd-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="3ccfd-127">-PoolObject</span></span>
<span data-ttu-id="3ccfd-128">Det pool-objekt som innehåller volymen som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="3ccfd-128">The pool object containing the volume to remove</span></span>

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

### <span data-ttu-id="3ccfd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ccfd-129">-ResourceGroupName</span></span>
<span data-ttu-id="3ccfd-130">ANF-volymens resurs grupp</span><span class="sxs-lookup"><span data-stu-id="3ccfd-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="3ccfd-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ccfd-131">-ResourceId</span></span>
<span data-ttu-id="3ccfd-132">Resurs-ID för ANF volym</span><span class="sxs-lookup"><span data-stu-id="3ccfd-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="3ccfd-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3ccfd-133">-Confirm</span></span>
<span data-ttu-id="3ccfd-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3ccfd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ccfd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ccfd-135">-WhatIf</span></span>
<span data-ttu-id="3ccfd-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3ccfd-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ccfd-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3ccfd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ccfd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ccfd-138">CommonParameters</span></span>
<span data-ttu-id="3ccfd-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ccfd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ccfd-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ccfd-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ccfd-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ccfd-141">INPUTS</span></span>

### <span data-ttu-id="3ccfd-142">System. String</span><span class="sxs-lookup"><span data-stu-id="3ccfd-142">System.String</span></span>

### <span data-ttu-id="3ccfd-143">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="3ccfd-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="3ccfd-144">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="3ccfd-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="3ccfd-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ccfd-145">OUTPUTS</span></span>

### <span data-ttu-id="3ccfd-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3ccfd-146">System.Boolean</span></span>

## <span data-ttu-id="3ccfd-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ccfd-147">NOTES</span></span>

## <span data-ttu-id="3ccfd-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ccfd-148">RELATED LINKS</span></span>

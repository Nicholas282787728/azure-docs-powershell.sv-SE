---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: 6ea65189969e38359bb6d4345ea4c47963f9eddf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389280"
---
# <span data-ttu-id="ea8f8-101">Remove-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="ea8f8-101">Remove-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="ea8f8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea8f8-102">SYNOPSIS</span></span>
<span data-ttu-id="ea8f8-103">Tar bort en ANF-ögonblicksbild (Azure NetApp filer).</span><span class="sxs-lookup"><span data-stu-id="ea8f8-103">Deletes an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="ea8f8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea8f8-104">SYNTAX</span></span>

### <span data-ttu-id="ea8f8-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ea8f8-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea8f8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea8f8-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea8f8-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea8f8-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea8f8-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea8f8-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -InputObject <PSNetAppFilesSnapshotPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea8f8-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea8f8-109">DESCRIPTION</span></span>
<span data-ttu-id="ea8f8-110">Cmdleten **Remove-AzNetAppFilesSnapshotPolicy** tar bort en ANF Snapshot-princip.</span><span class="sxs-lookup"><span data-stu-id="ea8f8-110">The **Remove-AzNetAppFilesSnapshotPolicy** cmdlet deletes an ANF snapshot policy.</span></span>

## <span data-ttu-id="ea8f8-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea8f8-111">EXAMPLES</span></span>

### <span data-ttu-id="ea8f8-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ea8f8-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="ea8f8-113">Det här kommandot tar bort den nya ANF säkerhets kopierings princip med namnet "MyBackupPolicy" för kontot "mitt konto".</span><span class="sxs-lookup"><span data-stu-id="ea8f8-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="ea8f8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea8f8-114">PARAMETERS</span></span>

### <span data-ttu-id="ea8f8-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ea8f8-115">-AccountName</span></span>
<span data-ttu-id="ea8f8-116">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="ea8f8-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="ea8f8-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="ea8f8-117">-AccountObject</span></span>
<span data-ttu-id="ea8f8-118">Kontot för det nya Snapshot policy-objektet</span><span class="sxs-lookup"><span data-stu-id="ea8f8-118">The Account for the new Snapshot Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea8f8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea8f8-119">-DefaultProfile</span></span>
<span data-ttu-id="ea8f8-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ea8f8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea8f8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea8f8-121">-InputObject</span></span>
<span data-ttu-id="ea8f8-122">SnapshotPolicy-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="ea8f8-122">The SnapshotPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea8f8-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="ea8f8-123">-Name</span></span>
<span data-ttu-id="ea8f8-124">Namnet på ANF</span><span class="sxs-lookup"><span data-stu-id="ea8f8-124">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8f8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea8f8-125">-PassThru</span></span>
<span data-ttu-id="ea8f8-126">Returnera om det angivna kontot har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ea8f8-126">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="ea8f8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea8f8-127">-ResourceGroupName</span></span>
<span data-ttu-id="ea8f8-128">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="ea8f8-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="ea8f8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea8f8-129">-ResourceId</span></span>
<span data-ttu-id="ea8f8-130">Resurs-ID för ANF</span><span class="sxs-lookup"><span data-stu-id="ea8f8-130">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="ea8f8-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ea8f8-131">-Confirm</span></span>
<span data-ttu-id="ea8f8-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ea8f8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea8f8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea8f8-133">-WhatIf</span></span>
<span data-ttu-id="ea8f8-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ea8f8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea8f8-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ea8f8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea8f8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea8f8-136">CommonParameters</span></span>
<span data-ttu-id="ea8f8-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea8f8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea8f8-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea8f8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea8f8-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea8f8-139">INPUTS</span></span>

### <span data-ttu-id="ea8f8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ea8f8-140">System.String</span></span>

### <span data-ttu-id="ea8f8-141">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="ea8f8-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="ea8f8-142">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="ea8f8-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="ea8f8-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea8f8-143">OUTPUTS</span></span>

### <span data-ttu-id="ea8f8-144">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="ea8f8-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="ea8f8-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea8f8-145">NOTES</span></span>

## <span data-ttu-id="ea8f8-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea8f8-146">RELATED LINKS</span></span>

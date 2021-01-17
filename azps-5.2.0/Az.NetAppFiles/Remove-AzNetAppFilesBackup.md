---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackup.md
ms.openlocfilehash: 34b4e43dcd09df600c73a6dd0a459a41b491da3d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410704"
---
# <span data-ttu-id="79e8f-101">Remove-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="79e8f-101">Remove-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="79e8f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79e8f-102">SYNOPSIS</span></span>
<span data-ttu-id="79e8f-103">Tar bort en ANF-säkerhetskopia (Azure NetApp filer).</span><span class="sxs-lookup"><span data-stu-id="79e8f-103">Deletes an Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="79e8f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79e8f-104">SYNTAX</span></span>

### <span data-ttu-id="79e8f-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="79e8f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackup -ResourceGroupName <String> [-AccountName <String>] -PoolName <String>
 [-VolumeName <String>] -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79e8f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79e8f-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -Name <String> -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79e8f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79e8f-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79e8f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79e8f-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -InputObject <PSNetAppFilesBackup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79e8f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79e8f-109">DESCRIPTION</span></span>
<span data-ttu-id="79e8f-110">Cmdleten **Remove-AzNetAppFilesBackup** tar bort ett ANF-konto.</span><span class="sxs-lookup"><span data-stu-id="79e8f-110">The **Remove-AzNetAppFilesBackup** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="79e8f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79e8f-111">EXAMPLES</span></span>

### <span data-ttu-id="79e8f-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="79e8f-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="79e8f-113">Det här kommandot tar bort den nya ANF säkerhets kopiering med namnet "min säkerhets kopiering" för volymen "volym".</span><span class="sxs-lookup"><span data-stu-id="79e8f-113">This command deletes the new ANF backup with a the name "MyBackup" for volume "MyVolume".</span></span>

## <span data-ttu-id="79e8f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79e8f-114">PARAMETERS</span></span>

### <span data-ttu-id="79e8f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="79e8f-115">-AccountName</span></span>
<span data-ttu-id="79e8f-116">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="79e8f-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="79e8f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79e8f-117">-DefaultProfile</span></span>
<span data-ttu-id="79e8f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="79e8f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79e8f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79e8f-119">-InputObject</span></span>
<span data-ttu-id="79e8f-120">Det SnapShot-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="79e8f-120">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79e8f-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="79e8f-121">-Name</span></span>
<span data-ttu-id="79e8f-122">Namnet på ANF säkerhets kopiering</span><span class="sxs-lookup"><span data-stu-id="79e8f-122">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79e8f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79e8f-123">-PassThru</span></span>
<span data-ttu-id="79e8f-124">Returnera om den angivna säkerhets kopian har tagits bort</span><span class="sxs-lookup"><span data-stu-id="79e8f-124">Return whether the specified backup was successfully removed</span></span>

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

### <span data-ttu-id="79e8f-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="79e8f-125">-PoolName</span></span>
<span data-ttu-id="79e8f-126">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="79e8f-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="79e8f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79e8f-127">-ResourceGroupName</span></span>
<span data-ttu-id="79e8f-128">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="79e8f-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="79e8f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79e8f-129">-ResourceId</span></span>
<span data-ttu-id="79e8f-130">Resurs-ID för ANF säkerhets kopiering</span><span class="sxs-lookup"><span data-stu-id="79e8f-130">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="79e8f-131">-Volym namn</span><span class="sxs-lookup"><span data-stu-id="79e8f-131">-VolumeName</span></span>
<span data-ttu-id="79e8f-132">Namnet på ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="79e8f-132">The name of the ANF volume</span></span>

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

### <span data-ttu-id="79e8f-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="79e8f-133">-VolumeObject</span></span>
<span data-ttu-id="79e8f-134">Volym objekt som innehåller säkerhets kopian som ska returneras</span><span class="sxs-lookup"><span data-stu-id="79e8f-134">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="79e8f-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="79e8f-135">-Confirm</span></span>
<span data-ttu-id="79e8f-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="79e8f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79e8f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79e8f-137">-WhatIf</span></span>
<span data-ttu-id="79e8f-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="79e8f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79e8f-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="79e8f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79e8f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79e8f-140">CommonParameters</span></span>
<span data-ttu-id="79e8f-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79e8f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79e8f-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79e8f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79e8f-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79e8f-143">INPUTS</span></span>

### <span data-ttu-id="79e8f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="79e8f-144">System.String</span></span>

### <span data-ttu-id="79e8f-145">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="79e8f-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="79e8f-146">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="79e8f-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="79e8f-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79e8f-147">OUTPUTS</span></span>

### <span data-ttu-id="79e8f-148">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="79e8f-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="79e8f-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79e8f-149">NOTES</span></span>

## <span data-ttu-id="79e8f-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79e8f-150">RELATED LINKS</span></span>

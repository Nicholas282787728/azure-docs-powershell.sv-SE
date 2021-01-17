---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
ms.openlocfilehash: a2cab03bb88d5b642a95142030eb646b2a5abef4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394656"
---
# <span data-ttu-id="4f0fe-101">Update-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="4f0fe-101">Update-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="4f0fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f0fe-102">SYNOPSIS</span></span>
<span data-ttu-id="4f0fe-103">Uppdaterar en Azure NetApp-fil (ANF) till de valfria modifierarna.</span><span class="sxs-lookup"><span data-stu-id="4f0fe-103">Updates an Azure NetApp Files (ANF) backup to the optional modifiers provided.</span></span>

## <span data-ttu-id="4f0fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f0fe-104">SYNTAX</span></span>

### <span data-ttu-id="4f0fe-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4f0fe-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolName <String> -VolumeName <String> [-Label <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f0fe-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f0fe-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup -Name <String> [-Label <String>] [-Tag <Hashtable>]
 -VolumeObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f0fe-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f0fe-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f0fe-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f0fe-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesBackup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f0fe-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f0fe-109">DESCRIPTION</span></span>
<span data-ttu-id="4f0fe-110">Cmdleten **Update-AzNetAppFilesBackup** ändrar en ANF-säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="4f0fe-110">The **Update-AzNetAppFilesBackup** cmdlet modifies an ANF backup.</span></span>

## <span data-ttu-id="4f0fe-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f0fe-111">EXAMPLES</span></span>

### <span data-ttu-id="4f0fe-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4f0fe-112">Example 1</span></span>
```powershell
PS C:\>  Update-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName $accName1 -Name $backupPolicyObject -Label "updatedLabel"
```

<span data-ttu-id="4f0fe-113">Det här kommandot utför en uppdatering av den angivna säkerhets kopian som ändrar det angivna användar namnet.</span><span class="sxs-lookup"><span data-stu-id="4f0fe-113">This command performs an update on the given backup modifying the username to that provided.</span></span>

## <span data-ttu-id="4f0fe-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f0fe-114">PARAMETERS</span></span>

### <span data-ttu-id="4f0fe-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4f0fe-115">-AccountName</span></span>
<span data-ttu-id="4f0fe-116">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="4f0fe-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="4f0fe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f0fe-117">-DefaultProfile</span></span>
<span data-ttu-id="4f0fe-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4f0fe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f0fe-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f0fe-119">-InputObject</span></span>
<span data-ttu-id="4f0fe-120">Det SnapShot-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="4f0fe-120">The snapshot object to remove</span></span>

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

### <span data-ttu-id="4f0fe-121">-Etikett</span><span class="sxs-lookup"><span data-stu-id="4f0fe-121">-Label</span></span>
<span data-ttu-id="4f0fe-122">Etikett för säkerhets kopiering</span><span class="sxs-lookup"><span data-stu-id="4f0fe-122">Label for backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f0fe-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="4f0fe-123">-Location</span></span>
<span data-ttu-id="4f0fe-124">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="4f0fe-124">The location of the resource</span></span>

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

### <span data-ttu-id="4f0fe-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="4f0fe-125">-Name</span></span>
<span data-ttu-id="4f0fe-126">Namnet på ANF säkerhets kopierings princip</span><span class="sxs-lookup"><span data-stu-id="4f0fe-126">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f0fe-127">-PoolName</span><span class="sxs-lookup"><span data-stu-id="4f0fe-127">-PoolName</span></span>
<span data-ttu-id="4f0fe-128">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="4f0fe-128">The name of the ANF pool</span></span>

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

### <span data-ttu-id="4f0fe-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f0fe-129">-ResourceGroupName</span></span>
<span data-ttu-id="4f0fe-130">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="4f0fe-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="4f0fe-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f0fe-131">-ResourceId</span></span>
<span data-ttu-id="4f0fe-132">Resurs-ID för ANF säkerhets kopiering</span><span class="sxs-lookup"><span data-stu-id="4f0fe-132">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="4f0fe-133">-Tagg</span><span class="sxs-lookup"><span data-stu-id="4f0fe-133">-Tag</span></span>
<span data-ttu-id="4f0fe-134">En hash som representerar resurs koder</span><span class="sxs-lookup"><span data-stu-id="4f0fe-134">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f0fe-135">-Volym namn</span><span class="sxs-lookup"><span data-stu-id="4f0fe-135">-VolumeName</span></span>
<span data-ttu-id="4f0fe-136">Namnet på ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="4f0fe-136">The name of the ANF volume</span></span>

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

### <span data-ttu-id="4f0fe-137">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="4f0fe-137">-VolumeObject</span></span>
<span data-ttu-id="4f0fe-138">Volym objekt som innehåller säkerhets kopian som ska returneras</span><span class="sxs-lookup"><span data-stu-id="4f0fe-138">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="4f0fe-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4f0fe-139">-Confirm</span></span>
<span data-ttu-id="4f0fe-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4f0fe-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f0fe-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f0fe-141">-WhatIf</span></span>
<span data-ttu-id="4f0fe-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4f0fe-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f0fe-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4f0fe-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f0fe-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f0fe-144">CommonParameters</span></span>
<span data-ttu-id="4f0fe-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f0fe-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f0fe-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f0fe-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f0fe-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f0fe-147">INPUTS</span></span>

### <span data-ttu-id="4f0fe-148">System. String</span><span class="sxs-lookup"><span data-stu-id="4f0fe-148">System.String</span></span>

### <span data-ttu-id="4f0fe-149">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="4f0fe-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="4f0fe-150">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="4f0fe-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="4f0fe-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f0fe-151">OUTPUTS</span></span>

### <span data-ttu-id="4f0fe-152">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="4f0fe-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="4f0fe-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f0fe-153">NOTES</span></span>

## <span data-ttu-id="4f0fe-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f0fe-154">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 0cebe34948984e36c9ad2fbe30de8da3a0e0ca92
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394651"
---
# <span data-ttu-id="f2868-101">Update-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="f2868-101">Update-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="f2868-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f2868-102">SYNOPSIS</span></span>
<span data-ttu-id="f2868-103">Uppdaterar en säkerhets kopierings princip för Azure NetApp-filer (ANF) till de valfria modifierarna.</span><span class="sxs-lookup"><span data-stu-id="f2868-103">Updates an Azure NetApp Files (ANF) backup policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="f2868-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f2868-104">SYNTAX</span></span>

### <span data-ttu-id="f2868-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f2868-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>]
 [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2868-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2868-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2868-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2868-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2868-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2868-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesBackupPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2868-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f2868-109">DESCRIPTION</span></span>
<span data-ttu-id="f2868-110">Cmdleten **Update-AzNetAppFilesBackupPolicy** ändrar en ANF säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="f2868-110">The **Update-AzNetAppFilesBackupPolicy** cmdlet modifies an ANF backup policy .</span></span>

## <span data-ttu-id="f2868-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f2868-111">EXAMPLES</span></span>

### <span data-ttu-id="f2868-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f2868-112">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy" -DailyBackupsToKeep 2
```

<span data-ttu-id="f2868-113">Det här kommandot ändrar säkerhets kopierings princip för ANF "MyBackupPolicy" så att angiven DailyBackupsToKeep visas.</span><span class="sxs-lookup"><span data-stu-id="f2868-113">This command changes the ANF backup policy "MyBackupPolicy" to have the given DailyBackupsToKeep.</span></span>

## <span data-ttu-id="f2868-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f2868-114">PARAMETERS</span></span>

### <span data-ttu-id="f2868-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f2868-115">-AccountName</span></span>
<span data-ttu-id="f2868-116">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="f2868-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="f2868-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="f2868-117">-AccountObject</span></span>
<span data-ttu-id="f2868-118">Det konto objekt som innehåller säkerhets kopierings principen</span><span class="sxs-lookup"><span data-stu-id="f2868-118">The Account object containing the Backup Policy to update</span></span>

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

### <span data-ttu-id="f2868-119">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="f2868-119">-DailyBackupsToKeep</span></span>
<span data-ttu-id="f2868-120">Dagliga säkerhets kopior för att hålla</span><span class="sxs-lookup"><span data-stu-id="f2868-120">Daily backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2868-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2868-121">-DefaultProfile</span></span>
<span data-ttu-id="f2868-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f2868-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2868-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2868-123">-InputObject</span></span>
<span data-ttu-id="f2868-124">BackupPolicy-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="f2868-124">The BackupPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2868-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="f2868-125">-Location</span></span>
<span data-ttu-id="f2868-126">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="f2868-126">The location of the resource</span></span>

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

### <span data-ttu-id="f2868-127">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="f2868-127">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="f2868-128">Månads vis säkerhets kopior för att hålla</span><span class="sxs-lookup"><span data-stu-id="f2868-128">Monthly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2868-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="f2868-129">-Name</span></span>
<span data-ttu-id="f2868-130">Namnet på ANF säkerhets kopierings princip</span><span class="sxs-lookup"><span data-stu-id="f2868-130">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="f2868-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2868-131">-ResourceGroupName</span></span>
<span data-ttu-id="f2868-132">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="f2868-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="f2868-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2868-133">-ResourceId</span></span>
<span data-ttu-id="f2868-134">Resurs-ID för ANF säkerhets kopierings princip</span><span class="sxs-lookup"><span data-stu-id="f2868-134">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="f2868-135">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f2868-135">-Tag</span></span>
<span data-ttu-id="f2868-136">En hash-matris som representerar resursfiler</span><span class="sxs-lookup"><span data-stu-id="f2868-136">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="f2868-137">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="f2868-137">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="f2868-138">Vecko antal säkerhets kopior som ska behållas</span><span class="sxs-lookup"><span data-stu-id="f2868-138">Weekly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2868-139">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="f2868-139">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="f2868-140">Årlig säkerhets kopiering för att hålla</span><span class="sxs-lookup"><span data-stu-id="f2868-140">Yearly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2868-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f2868-141">-Confirm</span></span>
<span data-ttu-id="f2868-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f2868-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2868-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2868-143">-WhatIf</span></span>
<span data-ttu-id="f2868-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f2868-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2868-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f2868-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2868-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2868-146">CommonParameters</span></span>
<span data-ttu-id="f2868-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2868-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2868-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2868-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2868-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f2868-149">INPUTS</span></span>

### <span data-ttu-id="f2868-150">System. String</span><span class="sxs-lookup"><span data-stu-id="f2868-150">System.String</span></span>

### <span data-ttu-id="f2868-151">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="f2868-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="f2868-152">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="f2868-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="f2868-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f2868-153">OUTPUTS</span></span>

### <span data-ttu-id="f2868-154">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="f2868-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="f2868-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f2868-155">NOTES</span></span>

## <span data-ttu-id="f2868-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f2868-156">RELATED LINKS</span></span>

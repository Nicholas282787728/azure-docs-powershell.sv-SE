---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: ce49a011ba7e6c746c97e4b1aca6273d7d8b650d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410747"
---
# <span data-ttu-id="b7095-101">New-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b7095-101">New-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="b7095-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b7095-102">SYNOPSIS</span></span>
<span data-ttu-id="b7095-103">Skapar en ny säkerhets kopierings princip för Azure NetApp (ANF) för ett ANF-konto.</span><span class="sxs-lookup"><span data-stu-id="b7095-103">Creates a new Azure NetApp Files (ANF) backup policy for an ANF account.</span></span>

## <span data-ttu-id="b7095-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b7095-104">SYNTAX</span></span>

### <span data-ttu-id="b7095-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b7095-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7095-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7095-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackupPolicy -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>]
 [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7095-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b7095-107">DESCRIPTION</span></span>
<span data-ttu-id="b7095-108">Cmdleten **New-AzNetAppFilesActiveDirectory** skapar en ny säkerhets kopierings princip för ett ANF-konto.</span><span class="sxs-lookup"><span data-stu-id="b7095-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new backup policy for an ANF account.</span></span>

## <span data-ttu-id="b7095-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b7095-109">EXAMPLES</span></span>

### <span data-ttu-id="b7095-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b7095-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyBackupPolicy" -Tag @{"tag1" = "tagValue"} -Enabled -DailyBackupsToKeep 1 -WeeklyBackupsToKeep 2 -MonthlyBackupsToKeep 2 -YearlyBackupsToKeep 1
```

<span data-ttu-id="b7095-111">Det här kommandot skapar den nya ANF säkerhets kopierings princip för ANF-kontot "mitt konto".</span><span class="sxs-lookup"><span data-stu-id="b7095-111">This command creates the new ANF backup policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="b7095-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b7095-112">PARAMETERS</span></span>

### <span data-ttu-id="b7095-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b7095-113">-AccountName</span></span>
<span data-ttu-id="b7095-114">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="b7095-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="b7095-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="b7095-115">-AccountObject</span></span>
<span data-ttu-id="b7095-116">Konto objekt för den nya säkerhets kopierings principen</span><span class="sxs-lookup"><span data-stu-id="b7095-116">The Account object for the new Backup Policy</span></span>

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

### <span data-ttu-id="b7095-117">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="b7095-117">-DailyBackupsToKeep</span></span>
<span data-ttu-id="b7095-118">Dagliga säkerhets kopior för att hålla</span><span class="sxs-lookup"><span data-stu-id="b7095-118">Daily backups count to keep</span></span>

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

### <span data-ttu-id="b7095-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7095-119">-DefaultProfile</span></span>
<span data-ttu-id="b7095-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b7095-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7095-121">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="b7095-121">-Enabled</span></span>
<span data-ttu-id="b7095-122">Den egenskap som ska väljas är aktive rad eller inte</span><span class="sxs-lookup"><span data-stu-id="b7095-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="b7095-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="b7095-123">-Location</span></span>
<span data-ttu-id="b7095-124">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="b7095-124">The location of the resource</span></span>

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

### <span data-ttu-id="b7095-125">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="b7095-125">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="b7095-126">Månads vis säkerhets kopior för att hålla</span><span class="sxs-lookup"><span data-stu-id="b7095-126">Monthly backups count to keep</span></span>

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

### <span data-ttu-id="b7095-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="b7095-127">-Name</span></span>
<span data-ttu-id="b7095-128">Namnet på ANF säkerhets kopierings princip</span><span class="sxs-lookup"><span data-stu-id="b7095-128">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7095-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7095-129">-ResourceGroupName</span></span>
<span data-ttu-id="b7095-130">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="b7095-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="b7095-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b7095-131">-Tag</span></span>
<span data-ttu-id="b7095-132">En hash-matris som representerar resursfiler</span><span class="sxs-lookup"><span data-stu-id="b7095-132">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="b7095-133">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="b7095-133">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="b7095-134">Vecko antal säkerhets kopior som ska behållas</span><span class="sxs-lookup"><span data-stu-id="b7095-134">Weekly backups count to keep</span></span>

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

### <span data-ttu-id="b7095-135">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="b7095-135">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="b7095-136">Årlig säkerhets kopiering för att hålla</span><span class="sxs-lookup"><span data-stu-id="b7095-136">Yearly backups count to keep</span></span>

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

### <span data-ttu-id="b7095-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b7095-137">-Confirm</span></span>
<span data-ttu-id="b7095-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b7095-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7095-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7095-139">-WhatIf</span></span>
<span data-ttu-id="b7095-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b7095-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7095-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b7095-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7095-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7095-142">CommonParameters</span></span>
<span data-ttu-id="b7095-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7095-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7095-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7095-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7095-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b7095-145">INPUTS</span></span>

### <span data-ttu-id="b7095-146">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="b7095-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="b7095-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b7095-147">OUTPUTS</span></span>

### <span data-ttu-id="b7095-148">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b7095-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="b7095-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b7095-149">NOTES</span></span>

## <span data-ttu-id="b7095-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b7095-150">RELATED LINKS</span></span>

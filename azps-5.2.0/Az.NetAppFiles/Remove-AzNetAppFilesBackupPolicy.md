---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 975e451854a935034dc4ed508770f48e126807e8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410683"
---
# <span data-ttu-id="f90bc-101">Remove-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="f90bc-101">Remove-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="f90bc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f90bc-102">SYNOPSIS</span></span>
<span data-ttu-id="f90bc-103">Tar bort en princip för säkerhets kopiering av Azure NetApp-filer (ANF).</span><span class="sxs-lookup"><span data-stu-id="f90bc-103">Deletes an Azure NetApp Files (ANF) backup policy.</span></span>

## <span data-ttu-id="f90bc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f90bc-104">SYNTAX</span></span>

### <span data-ttu-id="f90bc-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f90bc-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f90bc-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f90bc-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f90bc-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f90bc-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f90bc-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f90bc-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -InputObject <PSNetAppFilesBackupPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f90bc-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f90bc-109">DESCRIPTION</span></span>
<span data-ttu-id="f90bc-110">Cmdleten **Remove-AzNetAppFilesBackupPolicy** tar bort en ANF säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="f90bc-110">The **Remove-AzNetAppFilesBackupPolicy** cmdlet deletes an ANF backup policy.</span></span>

## <span data-ttu-id="f90bc-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f90bc-111">EXAMPLES</span></span>

### <span data-ttu-id="f90bc-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f90bc-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="f90bc-113">Det här kommandot tar bort den nya ANF säkerhets kopierings princip med namnet "MyBackupPolicy" för kontot "mitt konto".</span><span class="sxs-lookup"><span data-stu-id="f90bc-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="f90bc-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f90bc-114">PARAMETERS</span></span>

### <span data-ttu-id="f90bc-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f90bc-115">-AccountName</span></span>
<span data-ttu-id="f90bc-116">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="f90bc-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="f90bc-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="f90bc-117">-AccountObject</span></span>
<span data-ttu-id="f90bc-118">Det konto objekt som innehåller säkerhets kopierings principen som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="f90bc-118">The Account object containing the Backup Policy to remove</span></span>

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

### <span data-ttu-id="f90bc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f90bc-119">-DefaultProfile</span></span>
<span data-ttu-id="f90bc-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f90bc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f90bc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f90bc-121">-InputObject</span></span>
<span data-ttu-id="f90bc-122">BackupPolicy-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="f90bc-122">The BackupPolicy object to remove</span></span>

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

### <span data-ttu-id="f90bc-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="f90bc-123">-Name</span></span>
<span data-ttu-id="f90bc-124">Namnet på ANF säkerhets kopierings princip</span><span class="sxs-lookup"><span data-stu-id="f90bc-124">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="f90bc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f90bc-125">-PassThru</span></span>
<span data-ttu-id="f90bc-126">Returnera om den angivna säkerhets kopierings principen har tagits bort</span><span class="sxs-lookup"><span data-stu-id="f90bc-126">Return whether the specified backup policy was successfully removed</span></span>

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

### <span data-ttu-id="f90bc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f90bc-127">-ResourceGroupName</span></span>
<span data-ttu-id="f90bc-128">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="f90bc-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="f90bc-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f90bc-129">-ResourceId</span></span>
<span data-ttu-id="f90bc-130">Resurs-ID för ANF säkerhets kopierings princip</span><span class="sxs-lookup"><span data-stu-id="f90bc-130">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="f90bc-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f90bc-131">-Confirm</span></span>
<span data-ttu-id="f90bc-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f90bc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f90bc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f90bc-133">-WhatIf</span></span>
<span data-ttu-id="f90bc-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f90bc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f90bc-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f90bc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f90bc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f90bc-136">CommonParameters</span></span>
<span data-ttu-id="f90bc-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f90bc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f90bc-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f90bc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f90bc-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f90bc-139">INPUTS</span></span>

### <span data-ttu-id="f90bc-140">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="f90bc-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="f90bc-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f90bc-141">System.String</span></span>

### <span data-ttu-id="f90bc-142">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="f90bc-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="f90bc-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f90bc-143">OUTPUTS</span></span>

### <span data-ttu-id="f90bc-144">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="f90bc-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="f90bc-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f90bc-145">NOTES</span></span>

## <span data-ttu-id="f90bc-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f90bc-146">RELATED LINKS</span></span>

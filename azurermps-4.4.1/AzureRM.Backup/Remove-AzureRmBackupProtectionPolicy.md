---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 189E3DD8-AA43-4D4C-A873-971E0585E54E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 80b03c8ba4bab5968e55dff40633b014a586d450
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578504"
---
# <span data-ttu-id="75a2b-101">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="75a2b-101">Remove-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="75a2b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75a2b-102">SYNOPSIS</span></span>
<span data-ttu-id="75a2b-103">Tar bort en princip från ett säkerhets kopierings valv.</span><span class="sxs-lookup"><span data-stu-id="75a2b-103">Deletes a policy from a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75a2b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75a2b-104">SYNTAX</span></span>

```
Remove-AzureRmBackupProtectionPolicy [-Force] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75a2b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75a2b-105">DESCRIPTION</span></span>
<span data-ttu-id="75a2b-106">Cmdleten **Remove-AzureRmBackupProtectionPolicy** tar bort en princip från ett Azure Backup-valv.</span><span class="sxs-lookup"><span data-stu-id="75a2b-106">The **Remove-AzureRmBackupProtectionPolicy** cmdlet deletes a policy from an Azure Backup vault.</span></span>

<span data-ttu-id="75a2b-107">Innan du kan ta bort en säkerhets kopierings princip får principen inte ha associerade säkerhets kopierings objekt.</span><span class="sxs-lookup"><span data-stu-id="75a2b-107">Before you can delete a backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="75a2b-108">Innan du tar bort principen bör du kontrol lera att varje associerat objekt är kopplat till någon annan princip.</span><span class="sxs-lookup"><span data-stu-id="75a2b-108">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="75a2b-109">Använd cmdleten Enable-AzureRmBackupProtection om du vill koppla en annan princip till en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="75a2b-109">To associate another policy with a backup item, use the Enable-AzureRmBackupProtection cmdlet.</span></span>

## <span data-ttu-id="75a2b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75a2b-110">EXAMPLES</span></span>

### <span data-ttu-id="75a2b-111">Exempel 1: ta bort en princip för säkerhets kopiering</span><span class="sxs-lookup"><span data-stu-id="75a2b-111">Example 1: Remove a backup protection policy</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DailyBackup" | Remove-AzureRmBackupProtectionPolicy
```

<span data-ttu-id="75a2b-112">Det första kommandot får valvet med namnet Vault03 med hjälp av Get-AzureRmBackupVault cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75a2b-112">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="75a2b-113">Kommandot lagrar objektet i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="75a2b-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="75a2b-114">Med det andra kommandot skapas en bevarande princip för 30 dagar efter varje dag och sparas sedan i $Daily variabel.</span><span class="sxs-lookup"><span data-stu-id="75a2b-114">The second command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="75a2b-115">Det andra kommandot får skydds principen med namnet DailyBackup i valvet i $Vault med hjälp av cmdleten **Get-AzureRmBackupProtectionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="75a2b-115">The second command gets the protection policy named DailyBackup in the vault in $Vault by using the **Get-AzureRmBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="75a2b-116">Kommandot skickar principen till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="75a2b-116">The command passes the policy to the current cmdlet.</span></span>
<span data-ttu-id="75a2b-117">Denna cmdlet tar bort principen.</span><span class="sxs-lookup"><span data-stu-id="75a2b-117">That cmdlet removes the policy.</span></span>

## <span data-ttu-id="75a2b-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75a2b-118">PARAMETERS</span></span>

### <span data-ttu-id="75a2b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="75a2b-119">-Force</span></span>
<span data-ttu-id="75a2b-120">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="75a2b-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="75a2b-121">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="75a2b-121">-ProtectionPolicy</span></span>
<span data-ttu-id="75a2b-122">Anger skydds princip för den här cmdleten som tas bort.</span><span class="sxs-lookup"><span data-stu-id="75a2b-122">Specifies protection policy that this cmdlet removes.</span></span>
<span data-ttu-id="75a2b-123">För att få en **AzureRmBackupProtectionPolicy** , Använd cmdleten Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="75a2b-123">To obtain an **AzureRmBackupProtectionPolicy** , use the Get-AzureRmBackupProtectionPolicy cmdlet</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75a2b-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="75a2b-124">-Confirm</span></span>
<span data-ttu-id="75a2b-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="75a2b-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a2b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75a2b-126">-WhatIf</span></span>
<span data-ttu-id="75a2b-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="75a2b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75a2b-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="75a2b-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a2b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a2b-129">-DefaultProfile</span></span>
<span data-ttu-id="75a2b-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75a2b-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a2b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a2b-131">CommonParameters</span></span>
<span data-ttu-id="75a2b-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75a2b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a2b-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75a2b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a2b-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75a2b-134">INPUTS</span></span>

### <span data-ttu-id="75a2b-135">AzureRMBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="75a2b-135">AzureRMBackupProtectionPolicy</span></span>

## <span data-ttu-id="75a2b-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75a2b-136">OUTPUTS</span></span>

### <span data-ttu-id="75a2b-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="75a2b-137">None</span></span>

## <span data-ttu-id="75a2b-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75a2b-138">NOTES</span></span>

## <span data-ttu-id="75a2b-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75a2b-139">RELATED LINKS</span></span>

[<span data-ttu-id="75a2b-140">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="75a2b-140">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="75a2b-141">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="75a2b-141">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="75a2b-142">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="75a2b-142">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)



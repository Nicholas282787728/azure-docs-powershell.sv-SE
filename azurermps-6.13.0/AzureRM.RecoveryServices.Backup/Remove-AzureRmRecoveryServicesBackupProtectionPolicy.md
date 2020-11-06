---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/remove-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 805deece859eb4baa05d8c3d34dfcc8a9d571354
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584868"
---
# <span data-ttu-id="ff864-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ff864-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="ff864-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff864-102">SYNOPSIS</span></span>
<span data-ttu-id="ff864-103">Tar bort en säkerhets kopierings princip från ett valv.</span><span class="sxs-lookup"><span data-stu-id="ff864-103">Deletes a Backup protection policy from a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff864-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff864-104">SYNTAX</span></span>

### <span data-ttu-id="ff864-105">PolicyName (standard)</span><span class="sxs-lookup"><span data-stu-id="ff864-105">PolicyName (Default)</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff864-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="ff864-106">PolicyObject</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff864-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff864-107">DESCRIPTION</span></span>
<span data-ttu-id="ff864-108">Cmdleten **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** tar bort säkerhets kopierings principer för ett valv.</span><span class="sxs-lookup"><span data-stu-id="ff864-108">The **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="ff864-109">Innan du kan ta bort en säkerhets kopierings princip får principen inte ha associerade säkerhets kopierings objekt.</span><span class="sxs-lookup"><span data-stu-id="ff864-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="ff864-110">Innan du tar bort principen bör du kontrol lera att varje associerat objekt är kopplat till någon annan princip.</span><span class="sxs-lookup"><span data-stu-id="ff864-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="ff864-111">Använd cmdleten Enable-AzureRmRecoveryServicesBackupProtection om du vill koppla en annan princip till en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="ff864-111">To associate another policy with a Backup item, use the Enable-AzureRmRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="ff864-112">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ff864-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="ff864-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff864-113">EXAMPLES</span></span>

### <span data-ttu-id="ff864-114">Exempel 1: ta bort en princip</span><span class="sxs-lookup"><span data-stu-id="ff864-114">Example 1: Remove a policy</span></span>
```
PS C:\>$Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="ff864-115">Det första kommandot får säkerhets kopierings principen med namnet NewPolicy och lagrar den sedan i $Pol variabel.</span><span class="sxs-lookup"><span data-stu-id="ff864-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="ff864-116">Det andra kommandot tar bort principobjektet i $Pol.</span><span class="sxs-lookup"><span data-stu-id="ff864-116">The second command removes the policy object in $Pol.</span></span>

## <span data-ttu-id="ff864-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff864-117">PARAMETERS</span></span>

### <span data-ttu-id="ff864-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff864-118">-DefaultProfile</span></span>
<span data-ttu-id="ff864-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ff864-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff864-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ff864-120">-Force</span></span>
<span data-ttu-id="ff864-121">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ff864-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ff864-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="ff864-122">-Name</span></span>
<span data-ttu-id="ff864-123">Anger namnet på den säkerhets kopierings princip som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ff864-123">Specifies the name of the Backup protection policy to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff864-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff864-124">-PassThru</span></span>
<span data-ttu-id="ff864-125">Returnera den princip som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ff864-125">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="ff864-126">-Princip</span><span class="sxs-lookup"><span data-stu-id="ff864-126">-Policy</span></span>
<span data-ttu-id="ff864-127">Anger säkerhets kopierings principen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ff864-127">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="ff864-128">Använd Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet för att få ett **BackupPolicy** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ff864-128">To obtain an **BackupPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff864-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ff864-129">-VaultId</span></span>
<span data-ttu-id="ff864-130">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="ff864-130">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff864-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ff864-131">-Confirm</span></span>
<span data-ttu-id="ff864-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ff864-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff864-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff864-133">-WhatIf</span></span>
<span data-ttu-id="ff864-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ff864-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff864-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ff864-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff864-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff864-136">CommonParameters</span></span>
<span data-ttu-id="ff864-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff864-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff864-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff864-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff864-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff864-139">INPUTS</span></span>

### <span data-ttu-id="ff864-140">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="ff864-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>
<span data-ttu-id="ff864-141">Parametrar: princip (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ff864-141">Parameters: Policy (ByValue)</span></span>

### <span data-ttu-id="ff864-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ff864-142">System.String</span></span>
<span data-ttu-id="ff864-143">Parametrar: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ff864-143">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="ff864-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff864-144">OUTPUTS</span></span>

### <span data-ttu-id="ff864-145">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="ff864-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="ff864-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff864-146">NOTES</span></span>

## <span data-ttu-id="ff864-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff864-147">RELATED LINKS</span></span>

[<span data-ttu-id="ff864-148">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ff864-148">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="ff864-149">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ff864-149">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="ff864-150">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ff864-150">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)



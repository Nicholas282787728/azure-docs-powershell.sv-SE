---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: c3f4bb9b7c3d2b862ff78fdb35517f5837ffedf0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258046"
---
# <span data-ttu-id="4dc4b-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4dc4b-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="4dc4b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4dc4b-102">SYNOPSIS</span></span>
<span data-ttu-id="4dc4b-103">Tar bort en säkerhets kopierings princip från ett valv.</span><span class="sxs-lookup"><span data-stu-id="4dc4b-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="4dc4b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4dc4b-104">SYNTAX</span></span>

### <span data-ttu-id="4dc4b-105">PolicyName (standard)</span><span class="sxs-lookup"><span data-stu-id="4dc4b-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dc4b-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="4dc4b-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dc4b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4dc4b-107">DESCRIPTION</span></span>
<span data-ttu-id="4dc4b-108">Cmdleten **Remove-AzRecoveryServicesBackupProtectionPolicy** tar bort säkerhets kopierings principer för ett valv.</span><span class="sxs-lookup"><span data-stu-id="4dc4b-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="4dc4b-109">Innan du kan ta bort en säkerhets kopierings princip får principen inte ha associerade säkerhets kopierings objekt.</span><span class="sxs-lookup"><span data-stu-id="4dc4b-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="4dc4b-110">Innan du tar bort principen bör du kontrol lera att varje associerat objekt är kopplat till någon annan princip.</span><span class="sxs-lookup"><span data-stu-id="4dc4b-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="4dc4b-111">Använd cmdleten Enable-AzRecoveryServicesBackupProtection om du vill koppla en annan princip till en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="4dc4b-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="4dc4b-112">Ställ in valv kontexten med hjälp av Set-AzRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4dc4b-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="4dc4b-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4dc4b-113">EXAMPLES</span></span>

### <span data-ttu-id="4dc4b-114">Exempel 1: ta bort en princip</span><span class="sxs-lookup"><span data-stu-id="4dc4b-114">Example 1: Remove a policy</span></span>
```powershell
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="4dc4b-115">Det första kommandot får säkerhets kopierings principen med namnet NewPolicy och lagrar den sedan i $Pol variabel.</span><span class="sxs-lookup"><span data-stu-id="4dc4b-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="4dc4b-116">Det andra kommandot tar bort principobjektet i $Pol.</span><span class="sxs-lookup"><span data-stu-id="4dc4b-116">The second command removes the policy object in $Pol.</span></span>

### <span data-ttu-id="4dc4b-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4dc4b-117">Example 2</span></span>

<span data-ttu-id="4dc4b-118">Tar bort en säkerhets kopierings princip från ett valv.</span><span class="sxs-lookup"><span data-stu-id="4dc4b-118">Deletes a Backup protection policy from a vault.</span></span> <span data-ttu-id="4dc4b-119">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="4dc4b-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Remove-AzRecoveryServicesBackupProtectionPolicy -Name 'V2VM' -VaultId $vault.ID
```

## <span data-ttu-id="4dc4b-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4dc4b-120">PARAMETERS</span></span>

### <span data-ttu-id="4dc4b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dc4b-121">-DefaultProfile</span></span>
<span data-ttu-id="4dc4b-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4dc4b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4dc4b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="4dc4b-123">-Force</span></span>
<span data-ttu-id="4dc4b-124">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4dc4b-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4dc4b-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="4dc4b-125">-Name</span></span>
<span data-ttu-id="4dc4b-126">Anger namnet på den säkerhets kopierings princip som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4dc4b-126">Specifies the name of the Backup protection policy to remove.</span></span>

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

### <span data-ttu-id="4dc4b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4dc4b-127">-PassThru</span></span>
<span data-ttu-id="4dc4b-128">Returnera den princip som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4dc4b-128">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="4dc4b-129">-Princip</span><span class="sxs-lookup"><span data-stu-id="4dc4b-129">-Policy</span></span>
<span data-ttu-id="4dc4b-130">Anger säkerhets kopierings principen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4dc4b-130">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="4dc4b-131">Använd Get-AzRecoveryServicesBackupProtectionPolicy cmdlet för att få ett **BackupPolicy** -objekt.</span><span class="sxs-lookup"><span data-stu-id="4dc4b-131">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="4dc4b-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4dc4b-132">-VaultId</span></span>
<span data-ttu-id="4dc4b-133">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="4dc4b-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4dc4b-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4dc4b-134">-Confirm</span></span>
<span data-ttu-id="4dc4b-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4dc4b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dc4b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dc4b-136">-WhatIf</span></span>
<span data-ttu-id="4dc4b-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4dc4b-137">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="4dc4b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dc4b-138">CommonParameters</span></span>
<span data-ttu-id="4dc4b-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dc4b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dc4b-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4dc4b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dc4b-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4dc4b-141">INPUTS</span></span>

### <span data-ttu-id="4dc4b-142">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="4dc4b-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="4dc4b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4dc4b-143">System.String</span></span>

## <span data-ttu-id="4dc4b-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4dc4b-144">OUTPUTS</span></span>

### <span data-ttu-id="4dc4b-145">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="4dc4b-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="4dc4b-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4dc4b-146">NOTES</span></span>

## <span data-ttu-id="4dc4b-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4dc4b-147">RELATED LINKS</span></span>

[<span data-ttu-id="4dc4b-148">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4dc4b-148">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="4dc4b-149">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4dc4b-149">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="4dc4b-150">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4dc4b-150">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


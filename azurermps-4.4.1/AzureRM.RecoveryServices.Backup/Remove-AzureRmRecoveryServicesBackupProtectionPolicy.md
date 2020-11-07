---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 22dcc7459c0e574e62f3c87745ad6283fd919386
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575907"
---
# <span data-ttu-id="b446f-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b446f-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="b446f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b446f-102">SYNOPSIS</span></span>
<span data-ttu-id="b446f-103">Tar bort en säkerhets kopierings princip från ett valv.</span><span class="sxs-lookup"><span data-stu-id="b446f-103">Deletes a Backup protection policy from a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b446f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b446f-104">SYNTAX</span></span>

### <span data-ttu-id="b446f-105">PolicyName (standard)</span><span class="sxs-lookup"><span data-stu-id="b446f-105">PolicyName (Default)</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b446f-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="b446f-106">PolicyObject</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b446f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b446f-107">DESCRIPTION</span></span>
<span data-ttu-id="b446f-108">Cmdleten **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** tar bort säkerhets kopierings principer för ett valv.</span><span class="sxs-lookup"><span data-stu-id="b446f-108">The **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>

<span data-ttu-id="b446f-109">Innan du kan ta bort en säkerhets kopierings princip får principen inte ha associerade säkerhets kopierings objekt.</span><span class="sxs-lookup"><span data-stu-id="b446f-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="b446f-110">Innan du tar bort principen bör du kontrol lera att varje associerat objekt är kopplat till någon annan princip.</span><span class="sxs-lookup"><span data-stu-id="b446f-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="b446f-111">Använd cmdleten Enable-AzureRmRecoveryServicesBackupProtection om du vill koppla en annan princip till en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="b446f-111">To associate another policy with a Backup item, use the Enable-AzureRmRecoveryServicesBackupProtection cmdlet.</span></span>

<span data-ttu-id="b446f-112">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b446f-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="b446f-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b446f-113">EXAMPLES</span></span>

### <span data-ttu-id="b446f-114">Exempel 1: ta bort en princip</span><span class="sxs-lookup"><span data-stu-id="b446f-114">Example 1: Remove a policy</span></span>
```
PS C:\>$Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="b446f-115">Det första kommandot får säkerhets kopierings principen med namnet NewPolicy och lagrar den sedan i $Pol variabel.</span><span class="sxs-lookup"><span data-stu-id="b446f-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="b446f-116">Det andra kommandot tar bort principobjektet i $Pol.</span><span class="sxs-lookup"><span data-stu-id="b446f-116">The second command removes the policy object in $Pol.</span></span>

## <span data-ttu-id="b446f-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b446f-117">PARAMETERS</span></span>

### <span data-ttu-id="b446f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b446f-118">-Force</span></span>
<span data-ttu-id="b446f-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b446f-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b446f-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="b446f-120">-Name</span></span>
<span data-ttu-id="b446f-121">Anger namnet på den säkerhets kopierings princip som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b446f-121">Specifies the name of the Backup protection policy to remove.</span></span>

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

### <span data-ttu-id="b446f-122">-Princip</span><span class="sxs-lookup"><span data-stu-id="b446f-122">-Policy</span></span>
<span data-ttu-id="b446f-123">Anger säkerhets kopierings principen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b446f-123">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="b446f-124">Använd Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet för att få ett **BackupPolicy** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b446f-124">To obtain an **BackupPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="b446f-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b446f-125">-Confirm</span></span>
<span data-ttu-id="b446f-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b446f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b446f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b446f-127">-WhatIf</span></span>
<span data-ttu-id="b446f-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b446f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b446f-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b446f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b446f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b446f-130">-DefaultProfile</span></span>
<span data-ttu-id="b446f-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b446f-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b446f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b446f-132">CommonParameters</span></span>
<span data-ttu-id="b446f-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b446f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b446f-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b446f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b446f-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b446f-135">INPUTS</span></span>

### <span data-ttu-id="b446f-136">PolicyBase</span><span class="sxs-lookup"><span data-stu-id="b446f-136">PolicyBase</span></span>
<span data-ttu-id="b446f-137">Parametern ' policy ' godkänner värdet av typen ' PolicyBase ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="b446f-137">Parameter 'Policy' accepts value of type 'PolicyBase' from the pipeline</span></span>

## <span data-ttu-id="b446f-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b446f-138">OUTPUTS</span></span>

## <span data-ttu-id="b446f-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b446f-139">NOTES</span></span>

## <span data-ttu-id="b446f-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b446f-140">RELATED LINKS</span></span>

[<span data-ttu-id="b446f-141">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b446f-141">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="b446f-142">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b446f-142">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="b446f-143">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b446f-143">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


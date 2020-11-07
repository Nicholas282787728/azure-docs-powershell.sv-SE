---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/enable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 357256d1c1a754915cbebc978e5c4ccf4440ccf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757048"
---
# <span data-ttu-id="56003-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="56003-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="56003-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="56003-102">SYNOPSIS</span></span>
<span data-ttu-id="56003-103">Aktiverar säkerhets kopiering av ett objekt med en angiven säkerhets policy för säkerhet.</span><span class="sxs-lookup"><span data-stu-id="56003-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56003-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="56003-104">SYNTAX</span></span>

### <span data-ttu-id="56003-105">AzureVMComputeEnableProtection (standard)</span><span class="sxs-lookup"><span data-stu-id="56003-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56003-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="56003-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56003-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="56003-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 -StorageAccountName <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56003-108">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="56003-108">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56003-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="56003-109">DESCRIPTION</span></span>
<span data-ttu-id="56003-110">Cmdleten **Enable-AzureRmRecoveryServicesBackupProtection** anger Azure säkerhets kopierings princip för ett objekt.</span><span class="sxs-lookup"><span data-stu-id="56003-110">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="56003-111">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="56003-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="56003-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="56003-112">EXAMPLES</span></span>

### <span data-ttu-id="56003-113">Exempel 1: Aktivera säkerhets kopierings skydd för ett objekt</span><span class="sxs-lookup"><span data-stu-id="56003-113">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="56003-114">Den första cmdleten får ett standard princip objekt och lagrar det sedan i $Pol variabel.</span><span class="sxs-lookup"><span data-stu-id="56003-114">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="56003-115">Den andra cmdleten ställer in säkerhets kopierings skydds principen för den virtuella dator ARM med namnet V2VM med principen i $Pol.</span><span class="sxs-lookup"><span data-stu-id="56003-115">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="56003-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="56003-116">PARAMETERS</span></span>

### <span data-ttu-id="56003-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56003-117">-DefaultProfile</span></span>
<span data-ttu-id="56003-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="56003-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56003-119">-Objekt</span><span class="sxs-lookup"><span data-stu-id="56003-119">-Item</span></span>
<span data-ttu-id="56003-120">Anger det säkerhets kopie objekt som denna cmdlet aktiverar skydd för.</span><span class="sxs-lookup"><span data-stu-id="56003-120">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="56003-121">För att få en **AzureRmRecoveryServicesBackupItem** , Använd cmdleten Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="56003-121">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: ModifyProtection
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56003-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="56003-122">-Name</span></span>
<span data-ttu-id="56003-123">Anger namnet på säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="56003-123">Specifies the name of the Backup item.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, AzureFileShareEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56003-124">-Princip</span><span class="sxs-lookup"><span data-stu-id="56003-124">-Policy</span></span>
<span data-ttu-id="56003-125">Anger skydds princip som denna cmdlet associerar med ett objekt.</span><span class="sxs-lookup"><span data-stu-id="56003-125">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="56003-126">Använd Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet för att få ett **AzureRmRecoveryServicesBackupProtectionPolicy** -objekt.</span><span class="sxs-lookup"><span data-stu-id="56003-126">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56003-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56003-127">-ResourceGroupName</span></span>
<span data-ttu-id="56003-128">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="56003-128">Specifies the name of the resource group.</span></span>
<span data-ttu-id="56003-129">Ange endast den här parametern för virtuella ARM datorer.</span><span class="sxs-lookup"><span data-stu-id="56003-129">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56003-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="56003-130">-ServiceName</span></span>
<span data-ttu-id="56003-131">Anger tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="56003-131">Specifies the service name.</span></span>
<span data-ttu-id="56003-132">Ange endast den här parametern för virtuella ASM-datorer.</span><span class="sxs-lookup"><span data-stu-id="56003-132">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56003-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="56003-133">-StorageAccountName</span></span>
<span data-ttu-id="56003-134">Azure File Share lagrings konto namn</span><span class="sxs-lookup"><span data-stu-id="56003-134">Azure file share storage account name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileShareEnableProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56003-135">-VaultId</span><span class="sxs-lookup"><span data-stu-id="56003-135">-VaultId</span></span>
<span data-ttu-id="56003-136">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="56003-136">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="56003-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="56003-137">-Confirm</span></span>
<span data-ttu-id="56003-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="56003-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56003-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56003-139">-WhatIf</span></span>
<span data-ttu-id="56003-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="56003-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56003-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="56003-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56003-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56003-142">CommonParameters</span></span>
<span data-ttu-id="56003-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56003-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56003-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56003-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56003-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="56003-145">INPUTS</span></span>

### <span data-ttu-id="56003-146">System. String</span><span class="sxs-lookup"><span data-stu-id="56003-146">System.String</span></span>
<span data-ttu-id="56003-147">Parametrar: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="56003-147">Parameters: VaultId (ByValue)</span></span>

### <span data-ttu-id="56003-148">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="56003-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="56003-149">Parametrar: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="56003-149">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="56003-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="56003-150">OUTPUTS</span></span>

### <span data-ttu-id="56003-151">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="56003-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="56003-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="56003-152">NOTES</span></span>

## <span data-ttu-id="56003-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="56003-153">RELATED LINKS</span></span>

[<span data-ttu-id="56003-154">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="56003-154">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="56003-155">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="56003-155">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)



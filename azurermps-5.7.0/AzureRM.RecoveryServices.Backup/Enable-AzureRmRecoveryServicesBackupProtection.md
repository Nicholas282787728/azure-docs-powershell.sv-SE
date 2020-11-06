---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/enable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: efe4392fd57c5cb0beb6731fefb83878001b489b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574243"
---
# <span data-ttu-id="f030b-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="f030b-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="f030b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f030b-102">SYNOPSIS</span></span>
<span data-ttu-id="f030b-103">Aktiverar säkerhets kopiering av ett objekt med en angiven säkerhets policy för säkerhet.</span><span class="sxs-lookup"><span data-stu-id="f030b-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f030b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f030b-104">SYNTAX</span></span>

### <span data-ttu-id="f030b-105">AzureVMComputeEnableProtection (standard)</span><span class="sxs-lookup"><span data-stu-id="f030b-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f030b-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="f030b-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f030b-107">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="f030b-107">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f030b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f030b-108">DESCRIPTION</span></span>
<span data-ttu-id="f030b-109">Cmdleten **Enable-AzureRmRecoveryServicesBackupProtection** anger Azure säkerhets kopierings princip för ett objekt.</span><span class="sxs-lookup"><span data-stu-id="f030b-109">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>

<span data-ttu-id="f030b-110">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f030b-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="f030b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f030b-111">EXAMPLES</span></span>

### <span data-ttu-id="f030b-112">Exempel 1: Aktivera säkerhets kopierings skydd för ett objekt</span><span class="sxs-lookup"><span data-stu-id="f030b-112">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="f030b-113">Den första cmdleten får ett standard princip objekt och lagrar det sedan i $Pol variabel.</span><span class="sxs-lookup"><span data-stu-id="f030b-113">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="f030b-114">Den andra cmdleten ställer in säkerhets kopierings skydds principen för den virtuella dator ARM med namnet V2VM med principen i $Pol.</span><span class="sxs-lookup"><span data-stu-id="f030b-114">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="f030b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f030b-115">PARAMETERS</span></span>

### <span data-ttu-id="f030b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f030b-116">-DefaultProfile</span></span>
<span data-ttu-id="f030b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f030b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f030b-118">-Objekt</span><span class="sxs-lookup"><span data-stu-id="f030b-118">-Item</span></span>
<span data-ttu-id="f030b-119">Anger det säkerhets kopie objekt som denna cmdlet aktiverar skydd för.</span><span class="sxs-lookup"><span data-stu-id="f030b-119">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="f030b-120">För att få en **AzureRmRecoveryServicesBackupItem** , Använd cmdleten Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="f030b-120">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: ItemBase
Parameter Sets: ModifyProtection
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f030b-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="f030b-121">-Name</span></span>
<span data-ttu-id="f030b-122">Anger namnet på säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="f030b-122">Specifies the name of the Backup item.</span></span>

```yaml
Type: String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f030b-123">-Princip</span><span class="sxs-lookup"><span data-stu-id="f030b-123">-Policy</span></span>
<span data-ttu-id="f030b-124">Anger skydds princip som denna cmdlet associerar med ett objekt.</span><span class="sxs-lookup"><span data-stu-id="f030b-124">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="f030b-125">Använd Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet för att få ett **AzureRmRecoveryServicesBackupProtectionPolicy** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f030b-125">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f030b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f030b-126">-ResourceGroupName</span></span>
<span data-ttu-id="f030b-127">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f030b-127">Specifies the name of the resource group.</span></span>
<span data-ttu-id="f030b-128">Ange endast den här parametern för virtuella ARM datorer.</span><span class="sxs-lookup"><span data-stu-id="f030b-128">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: AzureVMComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f030b-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f030b-129">-ServiceName</span></span>
<span data-ttu-id="f030b-130">Anger tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="f030b-130">Specifies the service name.</span></span>
<span data-ttu-id="f030b-131">Ange endast den här parametern för virtuella ASM-datorer.</span><span class="sxs-lookup"><span data-stu-id="f030b-131">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f030b-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f030b-132">-Confirm</span></span>
<span data-ttu-id="f030b-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f030b-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f030b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f030b-134">-WhatIf</span></span>
<span data-ttu-id="f030b-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f030b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f030b-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f030b-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f030b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f030b-137">CommonParameters</span></span>
<span data-ttu-id="f030b-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f030b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f030b-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f030b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f030b-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f030b-140">INPUTS</span></span>

### <span data-ttu-id="f030b-141">ItemBase</span><span class="sxs-lookup"><span data-stu-id="f030b-141">ItemBase</span></span>
<span data-ttu-id="f030b-142">Parametern ' item ' godkänner värdet av typen ' ItemBase ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f030b-142">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="f030b-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f030b-143">OUTPUTS</span></span>

### <span data-ttu-id="f030b-144">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="f030b-144">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="f030b-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f030b-145">NOTES</span></span>

## <span data-ttu-id="f030b-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f030b-146">RELATED LINKS</span></span>

[<span data-ttu-id="f030b-147">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="f030b-147">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="f030b-148">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f030b-148">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)



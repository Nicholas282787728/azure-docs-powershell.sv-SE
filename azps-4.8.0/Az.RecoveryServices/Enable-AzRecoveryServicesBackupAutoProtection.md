---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: e47ed3d2859a78837c57803789721005a5248204
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258055"
---
# <span data-ttu-id="01492-101">Enable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="01492-101">Enable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="01492-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="01492-102">SYNOPSIS</span></span>
<span data-ttu-id="01492-103">Cmdleten **Enable-AzRecoveryServicesBackupAutoProtection** konfigurerar automatiskt skydd av aktuella och framtida SQL-DBS inom den angivna instansen med den angivna policyn.</span><span class="sxs-lookup"><span data-stu-id="01492-103">The **Enable-AzRecoveryServicesBackupAutoProtection** cmdlet sets up automatic protection of current and any future SQL DBs within the given instance with the supplied policy.</span></span>

## <span data-ttu-id="01492-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="01492-104">SYNTAX</span></span>

```
Enable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Policy] <PolicyBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01492-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="01492-105">DESCRIPTION</span></span>
<span data-ttu-id="01492-106">Med det här kommandot kan användarna automatiskt skydda alla befintliga oskyddade SQL-DBs och alla databaser som läggs till senare med den angivna principen.</span><span class="sxs-lookup"><span data-stu-id="01492-106">This command allows users to automatically protect all existing unprotected SQL DBs and any DB which will be added later with the given policy.</span></span>  <span data-ttu-id="01492-107">Eftersom instruktionen är att säkerhetskopiera alla framtida DBs, utförs åtgärden på en SQLInstance nivå, och Azure Backup-tjänsten skannar sedan automatiskt skyddade behållare för nya DBs och skyddar dem automatiskt.</span><span class="sxs-lookup"><span data-stu-id="01492-107">Since the instruction is to back up all future DBs, the operation is done at a SQLInstance level, Azure backup service will then regularly scan auto-protected containers for any new DBs and automatically protect them.</span></span>

## <span data-ttu-id="01492-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="01492-108">EXAMPLES</span></span>

### <span data-ttu-id="01492-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="01492-109">Example 1</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultSQLPolicy"
PS C:\> $SQLInstance = Get-AzRecoveryServicesBackupProtectableItem -workloadType MSSQL -ItemType SQLInstance -VaultId $targetVault.ID -Name "MSSQLInstance" -ServerName "TestSQLServer" 
PS C:\> Enable-AzRecoveryServicesBackupAutoProtection -InputItem $SQLInstance -BackupManagementType AzureWorkload -WorkloadType MSSQL -Policy $Pol -VaultId $targetvault.ID 
```

<span data-ttu-id="01492-110">Den första cmdleten får ett standard princip objekt och lagrar det sedan i $Pol variabel.</span><span class="sxs-lookup"><span data-stu-id="01492-110">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="01492-111">Den andra cmdleten hämtar den relevanta SQLInstance som är ett skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="01492-111">The second cmdlet fetches the relevant SQLInstance which is a protectable item.</span></span> <span data-ttu-id="01492-112">Det tredje kommandot ställer in automatisk skydd för den här instansen med principen i $Pol.</span><span class="sxs-lookup"><span data-stu-id="01492-112">The 3rd command then sets up auto protection for this instance using the policy in $Pol.</span></span>

### <span data-ttu-id="01492-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="01492-113">Example 2</span></span>

<span data-ttu-id="01492-114">Med de här kommandona kan användarna automatiskt skydda alla befintliga oskyddade DBs och alla databaser som läggs till senare med den angivna principen.</span><span class="sxs-lookup"><span data-stu-id="01492-114">This commands allows users to automatically protect all existing unprotected DBs and any DB which will be added later with the given policy.</span></span> <span data-ttu-id="01492-115">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="01492-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupAutoProtection -BackupManagementType AzureVM -InputItem <ProtectableItemBase> -Policy $Pol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="01492-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="01492-116">PARAMETERS</span></span>

### <span data-ttu-id="01492-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="01492-117">-BackupManagementType</span></span>
<span data-ttu-id="01492-118">Den klass med resurser som skyddas.</span><span class="sxs-lookup"><span data-stu-id="01492-118">The class of resources being protected.</span></span> <span data-ttu-id="01492-119">För närvarande kan de värden som stöds för denna cmdlet vara monoklonal, AzureWorkload, AzureVM</span><span class="sxs-lookup"><span data-stu-id="01492-119">Currently the values supported for this cmdlet are MAB, AzureWorkload, AzureVM</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01492-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01492-120">-DefaultProfile</span></span>
<span data-ttu-id="01492-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="01492-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01492-122">-InputItem</span><span class="sxs-lookup"><span data-stu-id="01492-122">-InputItem</span></span>
<span data-ttu-id="01492-123">Anger det skydd bara objekt som kan överföras som indata.</span><span class="sxs-lookup"><span data-stu-id="01492-123">Specifies the protectable item object that can be passed as an input.</span></span> <span data-ttu-id="01492-124">Det aktuella värdet som stöds är ett protectableItem-objekt av typen "SQLInstance".</span><span class="sxs-lookup"><span data-stu-id="01492-124">The current supported value is a protectableItem object of type "SQLInstance".</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01492-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01492-125">-PassThru</span></span>
<span data-ttu-id="01492-126">Returnera resultatet för automatiskt skydd.</span><span class="sxs-lookup"><span data-stu-id="01492-126">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="01492-127">-Princip</span><span class="sxs-lookup"><span data-stu-id="01492-127">-Policy</span></span>
<span data-ttu-id="01492-128">Skydds princip objekt.</span><span class="sxs-lookup"><span data-stu-id="01492-128">Protection policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01492-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="01492-129">-VaultId</span></span>
<span data-ttu-id="01492-130">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="01492-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="01492-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="01492-131">-WorkloadType</span></span>
<span data-ttu-id="01492-132">Arbets belastnings typ för resursen.</span><span class="sxs-lookup"><span data-stu-id="01492-132">Workload type of the resource.</span></span> <span data-ttu-id="01492-133">De aktuella värdena är AzureVM, WindowsServer, MSSQL</span><span class="sxs-lookup"><span data-stu-id="01492-133">The current supported values are AzureVM, WindowsServer, MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01492-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="01492-134">-Confirm</span></span>
<span data-ttu-id="01492-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="01492-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01492-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01492-136">-WhatIf</span></span>
<span data-ttu-id="01492-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="01492-137">Shows what would happen if the cmdlet runs.</span></span>


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

### <span data-ttu-id="01492-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01492-138">CommonParameters</span></span>
<span data-ttu-id="01492-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01492-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01492-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01492-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01492-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="01492-141">INPUTS</span></span>

### <span data-ttu-id="01492-142">System. String</span><span class="sxs-lookup"><span data-stu-id="01492-142">System.String</span></span>

## <span data-ttu-id="01492-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="01492-143">OUTPUTS</span></span>

### <span data-ttu-id="01492-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="01492-144">System.Object</span></span>

## <span data-ttu-id="01492-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="01492-145">NOTES</span></span>

## <span data-ttu-id="01492-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="01492-146">RELATED LINKS</span></span>

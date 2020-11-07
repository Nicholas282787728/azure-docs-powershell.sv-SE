---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: a17c7b8addf1bf1218131e8e950185d9da6c22d0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747477"
---
# <span data-ttu-id="9dc2a-101">Enable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="9dc2a-101">Enable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="9dc2a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9dc2a-102">SYNOPSIS</span></span>
<span data-ttu-id="9dc2a-103">Med de här kommandona kan användarna automatiskt skydda alla befintliga oskyddade DBs och alla databaser som läggs till senare med den angivna principen.</span><span class="sxs-lookup"><span data-stu-id="9dc2a-103">This commands allows users to automatically protect all existing unprotected DBs and any DB which will be added later with the given policy.</span></span> <span data-ttu-id="9dc2a-104">Med Azure Backup-tjänsten skannar du regelbundet automatiskt skyddade behållare för nya DBs och skyddar dem automatiskt.</span><span class="sxs-lookup"><span data-stu-id="9dc2a-104">Azure backup service will then regularly scan auto-protected containers for any new DBs and automatically protect them.</span></span>

## <span data-ttu-id="9dc2a-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9dc2a-105">SYNTAX</span></span>

```
Enable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Policy] <PolicyBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9dc2a-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9dc2a-106">DESCRIPTION</span></span>
<span data-ttu-id="9dc2a-107">Cmdleten **Enable-AzRecoveryServicesBackupAutoProtection** anger Azure automatisk säkerhets kopierings princip för ett skydd objekt.</span><span class="sxs-lookup"><span data-stu-id="9dc2a-107">The **Enable-AzRecoveryServicesBackupAutoProtection** cmdlet sets Azure auto Backup protection policy on an protectable item.</span></span>

## <span data-ttu-id="9dc2a-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9dc2a-108">EXAMPLES</span></span>

### <span data-ttu-id="9dc2a-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9dc2a-109">Example 1</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer
PS C:\> Get-AzRecoveryServicesBackupProtectableItem -Container $container -WorkloadType "MSSQL" -ItemType "SQLInstance" | Enable-AzRecoveryServicesBackupAutoProtection -BackupManagementType "AzureWorkload" -WorkloadType "MSSQL" -Policy $Pol
```

<span data-ttu-id="9dc2a-110">Den första cmdleten får ett standard princip objekt och lagrar det sedan i $Pol variabel.</span><span class="sxs-lookup"><span data-stu-id="9dc2a-110">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="9dc2a-111">Den andra cmdleten ställer in säkerhets kopierings princip för AzureWorkload med principen i $Pol.</span><span class="sxs-lookup"><span data-stu-id="9dc2a-111">The second cmdlet sets the Backup protection policy for the AzureWorkload using the policy in $Pol.</span></span>

## <span data-ttu-id="9dc2a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9dc2a-112">PARAMETERS</span></span>

### <span data-ttu-id="9dc2a-113">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="9dc2a-113">-BackupManagementType</span></span>
<span data-ttu-id="9dc2a-114">Resurs för säkerhets kopierings hantering (till exempel: monoklonal, DPM, AzureWorkload).</span><span class="sxs-lookup"><span data-stu-id="9dc2a-114">Backup Management type of the resource (for example: MAB, DPM, AzureWorkload).</span></span>

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

### <span data-ttu-id="9dc2a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dc2a-115">-DefaultProfile</span></span>
<span data-ttu-id="9dc2a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9dc2a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dc2a-117">-InputItem</span><span class="sxs-lookup"><span data-stu-id="9dc2a-117">-InputItem</span></span>
<span data-ttu-id="9dc2a-118">Anger det skydd bara objekt som kan överföras som indata.</span><span class="sxs-lookup"><span data-stu-id="9dc2a-118">Specifies the protectable item object that can be passed as an input.</span></span>

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

### <span data-ttu-id="9dc2a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9dc2a-119">-PassThru</span></span>
<span data-ttu-id="9dc2a-120">Returnera resultatet för automatiskt skydd.</span><span class="sxs-lookup"><span data-stu-id="9dc2a-120">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="9dc2a-121">-Princip</span><span class="sxs-lookup"><span data-stu-id="9dc2a-121">-Policy</span></span>
<span data-ttu-id="9dc2a-122">Skydds princip objekt.</span><span class="sxs-lookup"><span data-stu-id="9dc2a-122">Protection policy object.</span></span>

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

### <span data-ttu-id="9dc2a-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="9dc2a-123">-VaultId</span></span>
<span data-ttu-id="9dc2a-124">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="9dc2a-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="9dc2a-125">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="9dc2a-125">-WorkloadType</span></span>
<span data-ttu-id="9dc2a-126">Resursens arbets typ (till exempel: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="9dc2a-126">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

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

### <span data-ttu-id="9dc2a-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9dc2a-127">-Confirm</span></span>
<span data-ttu-id="9dc2a-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9dc2a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dc2a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dc2a-129">-WhatIf</span></span>
<span data-ttu-id="9dc2a-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9dc2a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dc2a-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9dc2a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dc2a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dc2a-132">CommonParameters</span></span>
<span data-ttu-id="9dc2a-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dc2a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dc2a-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dc2a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dc2a-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9dc2a-135">INPUTS</span></span>

### <span data-ttu-id="9dc2a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9dc2a-136">System.String</span></span>

## <span data-ttu-id="9dc2a-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9dc2a-137">OUTPUTS</span></span>

### <span data-ttu-id="9dc2a-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="9dc2a-138">System.Object</span></span>

## <span data-ttu-id="9dc2a-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9dc2a-139">NOTES</span></span>

## <span data-ttu-id="9dc2a-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9dc2a-140">RELATED LINKS</span></span>
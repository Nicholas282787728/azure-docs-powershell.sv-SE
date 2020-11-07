---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: 97eae8c5c545297a7d6287a951ec02433d591168
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927709"
---
# <span data-ttu-id="53cfc-101">Disable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="53cfc-101">Disable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="53cfc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53cfc-102">SYNOPSIS</span></span>
<span data-ttu-id="53cfc-103">Inaktiverar automatisk säkerhets kopiering för ett skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="53cfc-103">Disables auto backup for a protectable item.</span></span>

## <span data-ttu-id="53cfc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53cfc-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53cfc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53cfc-105">DESCRIPTION</span></span>
<span data-ttu-id="53cfc-106">Cmdleten **disable-AzRecoveryServicesBackupAutoProtection** inaktiverar skyddet för ett skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="53cfc-106">The **Disable-AzRecoveryServicesBackupAutoProtection** cmdlet disables protection on a protectable item.</span></span>

## <span data-ttu-id="53cfc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53cfc-107">EXAMPLES</span></span>

### <span data-ttu-id="53cfc-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="53cfc-108">Example 1</span></span>
```
PS C:\> $container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer
PS C:\> Get-AzRecoveryServicesBackupProtectableItem -Container $container -WorkloadType "MSSQL" -ItemType "SQLInstance" | Disable-AzRecoveryServicesBackupAutoProtection -BackupManagementType "AzureWorkload" -WorkloadType "MSSQL"
```

<span data-ttu-id="53cfc-109">Den första cmdleten inaktiverar säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="53cfc-109">The first cmdlet disables the Backup protection policy.</span></span>

## <span data-ttu-id="53cfc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53cfc-110">PARAMETERS</span></span>

### <span data-ttu-id="53cfc-111">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="53cfc-111">-BackupManagementType</span></span>
<span data-ttu-id="53cfc-112">Resurs för säkerhets kopierings hantering (till exempel: monoklonal, DPM).</span><span class="sxs-lookup"><span data-stu-id="53cfc-112">Backup Management type of the resource (for example: MAB, DPM).</span></span>

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

### <span data-ttu-id="53cfc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53cfc-113">-DefaultProfile</span></span>
<span data-ttu-id="53cfc-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="53cfc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53cfc-115">-InputItem</span><span class="sxs-lookup"><span data-stu-id="53cfc-115">-InputItem</span></span>
<span data-ttu-id="53cfc-116">Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="53cfc-116">Item Id</span></span>

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

### <span data-ttu-id="53cfc-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53cfc-117">-PassThru</span></span>
<span data-ttu-id="53cfc-118">Returnera resultatet för automatiskt skydd.</span><span class="sxs-lookup"><span data-stu-id="53cfc-118">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="53cfc-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="53cfc-119">-VaultId</span></span>
<span data-ttu-id="53cfc-120">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="53cfc-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="53cfc-121">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="53cfc-121">-WorkloadType</span></span>
<span data-ttu-id="53cfc-122">Resursens arbets belastning (till exempel: AzureVM, WindowsServer, AzureFiles).</span><span class="sxs-lookup"><span data-stu-id="53cfc-122">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles).</span></span>

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

### <span data-ttu-id="53cfc-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="53cfc-123">-Confirm</span></span>
<span data-ttu-id="53cfc-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="53cfc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53cfc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53cfc-125">-WhatIf</span></span>
<span data-ttu-id="53cfc-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="53cfc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53cfc-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="53cfc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53cfc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53cfc-128">CommonParameters</span></span>
<span data-ttu-id="53cfc-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53cfc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53cfc-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53cfc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53cfc-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53cfc-131">INPUTS</span></span>

### <span data-ttu-id="53cfc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="53cfc-132">System.String</span></span>

## <span data-ttu-id="53cfc-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53cfc-133">OUTPUTS</span></span>

### <span data-ttu-id="53cfc-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="53cfc-134">System.Boolean</span></span>

## <span data-ttu-id="53cfc-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53cfc-135">NOTES</span></span>

## <span data-ttu-id="53cfc-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53cfc-136">RELATED LINKS</span></span>

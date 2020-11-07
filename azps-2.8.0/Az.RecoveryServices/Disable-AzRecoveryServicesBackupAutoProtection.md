---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: 2613761db4a975f1bd4e04458ccdc5df81c0a2d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919802"
---
# <span data-ttu-id="71967-101">Disable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="71967-101">Disable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="71967-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="71967-102">SYNOPSIS</span></span>
<span data-ttu-id="71967-103">Inaktiverar automatisk säkerhets kopiering för ett skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="71967-103">Disables auto backup for a protectable item.</span></span>

## <span data-ttu-id="71967-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="71967-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71967-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="71967-105">DESCRIPTION</span></span>
<span data-ttu-id="71967-106">Cmdleten **disable-AzRecoveryServicesBackupAutoProtection** inaktiverar skyddet för ett skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="71967-106">The **Disable-AzRecoveryServicesBackupAutoProtection** cmdlet disables protection on a protectable item.</span></span>

## <span data-ttu-id="71967-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="71967-107">EXAMPLES</span></span>

### <span data-ttu-id="71967-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="71967-108">Example 1</span></span>
```
PS C:\> $container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer
PS C:\> Get-AzRecoveryServicesBackupProtectableItem -Container $container -WorkloadType "MSSQL" -ItemType "SQLInstance" | Disable-AzRecoveryServicesBackupAutoProtection -BackupManagementType "AzureWorkload" -WorkloadType "MSSQL"
```

<span data-ttu-id="71967-109">Den första cmdleten inaktiverar säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="71967-109">The first cmdlet disables the Backup protection policy.</span></span>

## <span data-ttu-id="71967-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="71967-110">PARAMETERS</span></span>

### <span data-ttu-id="71967-111">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="71967-111">-BackupManagementType</span></span>
<span data-ttu-id="71967-112">Resurs för säkerhets kopierings hantering (till exempel: monoklonal, DPM).</span><span class="sxs-lookup"><span data-stu-id="71967-112">Backup Management type of the resource (for example: MAB, DPM).</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71967-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71967-113">-DefaultProfile</span></span>
<span data-ttu-id="71967-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="71967-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71967-115">-InputItem</span><span class="sxs-lookup"><span data-stu-id="71967-115">-InputItem</span></span>
<span data-ttu-id="71967-116">Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="71967-116">Item Id</span></span>

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

### <span data-ttu-id="71967-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71967-117">-PassThru</span></span>
<span data-ttu-id="71967-118">Returnera resultatet för automatiskt skydd.</span><span class="sxs-lookup"><span data-stu-id="71967-118">Return the result for auto protection.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71967-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="71967-119">-VaultId</span></span>
<span data-ttu-id="71967-120">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="71967-120">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71967-121">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="71967-121">-WorkloadType</span></span>
<span data-ttu-id="71967-122">Resursens arbets belastning (till exempel: AzureVM, WindowsServer, AzureFiles).</span><span class="sxs-lookup"><span data-stu-id="71967-122">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles).</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71967-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="71967-123">-Confirm</span></span>
<span data-ttu-id="71967-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="71967-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71967-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71967-125">-WhatIf</span></span>
<span data-ttu-id="71967-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="71967-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71967-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="71967-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71967-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71967-128">CommonParameters</span></span>
<span data-ttu-id="71967-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71967-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="71967-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71967-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71967-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="71967-131">INPUTS</span></span>

### <span data-ttu-id="71967-132">System. String</span><span class="sxs-lookup"><span data-stu-id="71967-132">System.String</span></span>

## <span data-ttu-id="71967-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="71967-133">OUTPUTS</span></span>

### <span data-ttu-id="71967-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="71967-134">System.Boolean</span></span>

## <span data-ttu-id="71967-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="71967-135">NOTES</span></span>

## <span data-ttu-id="71967-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="71967-136">RELATED LINKS</span></span>

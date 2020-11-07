---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: eeffbbd62a4c161b95004c6f4bd40d31fbd02517
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920214"
---
# <span data-ttu-id="a2036-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="a2036-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="a2036-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a2036-102">SYNOPSIS</span></span>
<span data-ttu-id="a2036-103">Med det här kommandot kan du använda Azure Backup för att konvertera resursen till en behållare för säkerhets kopior som sedan registreras för det angivna Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="a2036-103">This command allows Azure Backup to convert the �Resource� to a �Backup Container� which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="a2036-104">Med Azure Backup-tjänsten kan arbets belastningarna för den angivna arbets belastnings typen i den här behållaren skyddas senare.</span><span class="sxs-lookup"><span data-stu-id="a2036-104">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="a2036-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a2036-105">SYNTAX</span></span>

### <span data-ttu-id="a2036-106">Registrera dig (standard)</span><span class="sxs-lookup"><span data-stu-id="a2036-106">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2036-107">Registrera om</span><span class="sxs-lookup"><span data-stu-id="a2036-107">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2036-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a2036-108">DESCRIPTION</span></span>
<span data-ttu-id="a2036-109">Cmdleten registrerar en Azure VM för AzureWorkloads med specifika workloadType.</span><span class="sxs-lookup"><span data-stu-id="a2036-109">The cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="a2036-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a2036-110">EXAMPLES</span></span>

### <span data-ttu-id="a2036-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a2036-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="a2036-112">Cmdleten registrerar en Azure VM för arbets belastnings tjänsten MSSQL.</span><span class="sxs-lookup"><span data-stu-id="a2036-112">The cmdlet registers an azure VM for the workload MSSQL.</span></span>

## <span data-ttu-id="a2036-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a2036-113">PARAMETERS</span></span>

### <span data-ttu-id="a2036-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="a2036-114">-BackupManagementType</span></span>
<span data-ttu-id="a2036-115">Säkerhets kopierings hanterings typen för Azure Backup-behållaren</span><span class="sxs-lookup"><span data-stu-id="a2036-115">The backup management type of the Azure Backup container</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2036-116">-Container</span><span class="sxs-lookup"><span data-stu-id="a2036-116">-Container</span></span>
<span data-ttu-id="a2036-117">Behållare där objektet finns</span><span class="sxs-lookup"><span data-stu-id="a2036-117">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: ReRegister
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2036-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2036-118">-DefaultProfile</span></span>
<span data-ttu-id="a2036-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a2036-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2036-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a2036-120">-Force</span></span>
<span data-ttu-id="a2036-121">Tvinga register-behållare (förhindrar bekräftelse dialog rutan).</span><span class="sxs-lookup"><span data-stu-id="a2036-121">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="a2036-122">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="a2036-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="a2036-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2036-123">-ResourceId</span></span>
<span data-ttu-id="a2036-124">ID för Azure-resursen vars ombud måste kontrol leras om det redan skyddas av något RecoveryServices-valv i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="a2036-124">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Register
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2036-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a2036-125">-VaultId</span></span>
<span data-ttu-id="a2036-126">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="a2036-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a2036-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="a2036-127">-WorkloadType</span></span>
<span data-ttu-id="a2036-128">Resursens arbets typ (till exempel: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="a2036-128">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

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

### <span data-ttu-id="a2036-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a2036-129">-Confirm</span></span>
<span data-ttu-id="a2036-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a2036-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2036-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2036-131">-WhatIf</span></span>
<span data-ttu-id="a2036-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a2036-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2036-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a2036-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2036-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2036-134">CommonParameters</span></span>
<span data-ttu-id="a2036-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2036-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2036-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2036-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2036-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a2036-137">INPUTS</span></span>

### <span data-ttu-id="a2036-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a2036-138">System.String</span></span>

## <span data-ttu-id="a2036-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a2036-139">OUTPUTS</span></span>

### <span data-ttu-id="a2036-140">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="a2036-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="a2036-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a2036-141">NOTES</span></span>

## <span data-ttu-id="a2036-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a2036-142">RELATED LINKS</span></span>
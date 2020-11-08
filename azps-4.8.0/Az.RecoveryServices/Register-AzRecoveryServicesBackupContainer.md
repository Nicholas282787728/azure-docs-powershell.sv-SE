---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: cfa8abf93fcb7eb4cd3848b1a5f69cf28a5fe6ab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261977"
---
# <span data-ttu-id="bd690-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="bd690-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="bd690-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd690-102">SYNOPSIS</span></span>
<span data-ttu-id="bd690-103">**Register-AzRecoveryServicesBackupContainer** cmdlet registrerar en Azure VM för AzureWorkloads med specifika workloadType.</span><span class="sxs-lookup"><span data-stu-id="bd690-103">The **Register-AzRecoveryServicesBackupContainer** cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="bd690-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd690-104">SYNTAX</span></span>

### <span data-ttu-id="bd690-105">Registrera dig (standard)</span><span class="sxs-lookup"><span data-stu-id="bd690-105">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd690-106">Registrera om</span><span class="sxs-lookup"><span data-stu-id="bd690-106">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd690-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd690-107">DESCRIPTION</span></span>
<span data-ttu-id="bd690-108">Med det här kommandot kan du använda Azure Backup för att konvertera resursen till en behållare för säkerhets kopior som sedan registreras för det angivna Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="bd690-108">This command allows Azure Backup to convert the Resource to a Backup Container which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="bd690-109">Med Azure Backup-tjänsten kan arbets belastningarna för den angivna arbets belastnings typen i den här behållaren skyddas senare.</span><span class="sxs-lookup"><span data-stu-id="bd690-109">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="bd690-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd690-110">EXAMPLES</span></span>

### <span data-ttu-id="bd690-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bd690-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="bd690-112">Cmdleten registrerar en Azure VM som en behållare för tjänsten för arbets belastnings-MSSQL.</span><span class="sxs-lookup"><span data-stu-id="bd690-112">The cmdlet registers an azure VM as a container for the workload MSSQL.</span></span>

## <span data-ttu-id="bd690-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd690-113">PARAMETERS</span></span>

### <span data-ttu-id="bd690-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="bd690-114">-BackupManagementType</span></span>
<span data-ttu-id="bd690-115">Den klass med resurser som skyddas.</span><span class="sxs-lookup"><span data-stu-id="bd690-115">The class of resources being protected.</span></span> <span data-ttu-id="bd690-116">För närvarande är det värde som stöds för denna cmdlet AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="bd690-116">Currently the value supported for this cmdlet is AzureWorkload</span></span>

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

### <span data-ttu-id="bd690-117">-Container</span><span class="sxs-lookup"><span data-stu-id="bd690-117">-Container</span></span>
<span data-ttu-id="bd690-118">Behållare där objektet finns</span><span class="sxs-lookup"><span data-stu-id="bd690-118">Container where the item resides</span></span>

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

### <span data-ttu-id="bd690-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd690-119">-DefaultProfile</span></span>
<span data-ttu-id="bd690-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bd690-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd690-121">-Force</span><span class="sxs-lookup"><span data-stu-id="bd690-121">-Force</span></span>
<span data-ttu-id="bd690-122">Tvinga register-behållare (förhindrar bekräftelse dialog rutan).</span><span class="sxs-lookup"><span data-stu-id="bd690-122">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="bd690-123">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="bd690-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="bd690-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd690-124">-ResourceId</span></span>
<span data-ttu-id="bd690-125">ID för Azure-resursen vars ombud måste kontrol leras om det redan skyddas av något RecoveryServices-valv i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="bd690-125">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="bd690-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="bd690-126">-VaultId</span></span>
<span data-ttu-id="bd690-127">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="bd690-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="bd690-128">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="bd690-128">-WorkloadType</span></span>
<span data-ttu-id="bd690-129">Arbets belastnings typ för resursen.</span><span class="sxs-lookup"><span data-stu-id="bd690-129">Workload type of the resource.</span></span> <span data-ttu-id="bd690-130">Det aktuella värdet som stöds är AzureVM, WindowsServer, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="bd690-130">The current supported value is AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="bd690-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bd690-131">-Confirm</span></span>
<span data-ttu-id="bd690-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bd690-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd690-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd690-133">-WhatIf</span></span>
<span data-ttu-id="bd690-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bd690-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="bd690-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd690-135">CommonParameters</span></span>
<span data-ttu-id="bd690-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd690-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd690-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd690-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd690-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd690-138">INPUTS</span></span>

### <span data-ttu-id="bd690-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bd690-139">System.String</span></span>

## <span data-ttu-id="bd690-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd690-140">OUTPUTS</span></span>

### <span data-ttu-id="bd690-141">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="bd690-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="bd690-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd690-142">NOTES</span></span>

## <span data-ttu-id="bd690-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd690-143">RELATED LINKS</span></span>

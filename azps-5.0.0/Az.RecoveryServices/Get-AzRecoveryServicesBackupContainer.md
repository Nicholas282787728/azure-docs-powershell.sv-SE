---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: f061dc0f729709dee3bfe08bb22dba8d49a7f31b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322445"
---
# <span data-ttu-id="dfeda-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="dfeda-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="dfeda-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dfeda-102">SYNOPSIS</span></span>

<span data-ttu-id="dfeda-103">Hämtar säkerhets kopierings behållare.</span><span class="sxs-lookup"><span data-stu-id="dfeda-103">Gets Backup containers.</span></span>

## <span data-ttu-id="dfeda-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dfeda-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfeda-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dfeda-105">DESCRIPTION</span></span>

<span data-ttu-id="dfeda-106">Cmdleten **Get-AzRecoveryServicesBackupContainer** hämtar en behållare för säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="dfeda-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="dfeda-107">En säkerhets kopia kapslar in data källor som är utformat som säkerhets kopie objekt.</span><span class="sxs-lookup"><span data-stu-id="dfeda-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="dfeda-108">Ange valv kontexten med parametern-VaultId.</span><span class="sxs-lookup"><span data-stu-id="dfeda-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="dfeda-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dfeda-109">EXAMPLES</span></span>

### <span data-ttu-id="dfeda-110">Exempel 1: Hämta en specifik behållare</span><span class="sxs-lookup"><span data-stu-id="dfeda-110">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="dfeda-111">Det här kommandot hämtar behållaren med namnet V2VM av typen AzureVM.</span><span class="sxs-lookup"><span data-stu-id="dfeda-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="dfeda-112">Exempel 2: Hämta alla behållare av en viss typ</span><span class="sxs-lookup"><span data-stu-id="dfeda-112">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="dfeda-113">Det här kommandot får alla Windows-behållare som skyddas av Azure Backup-agenten.</span><span class="sxs-lookup"><span data-stu-id="dfeda-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="dfeda-114">Parametern **BackupManagementType** krävs endast för Windows-behållare.</span><span class="sxs-lookup"><span data-stu-id="dfeda-114">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="dfeda-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dfeda-115">PARAMETERS</span></span>

### <span data-ttu-id="dfeda-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="dfeda-116">-BackupManagementType</span></span>

<span data-ttu-id="dfeda-117">Den klass med resurser som skyddas.</span><span class="sxs-lookup"><span data-stu-id="dfeda-117">The class of resources being protected.</span></span> <span data-ttu-id="dfeda-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="dfeda-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dfeda-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="dfeda-119">AzureVM</span></span>
- <span data-ttu-id="dfeda-120">OM</span><span class="sxs-lookup"><span data-stu-id="dfeda-120">MARS</span></span>
- <span data-ttu-id="dfeda-121">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="dfeda-121">AzureWorkload</span></span>
- <span data-ttu-id="dfeda-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="dfeda-122">AzureStorage</span></span>

<span data-ttu-id="dfeda-123">Den här parametern används för att differentiera Windows-datorer som säkerhets kopie ras med MARS agent eller andra säkerhets kopierings motorer.</span><span class="sxs-lookup"><span data-stu-id="dfeda-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, AzureWorkload, AzureStorage

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfeda-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="dfeda-124">-ContainerType</span></span>

<span data-ttu-id="dfeda-125">Anger typ av säkerhets kopierings behållare.</span><span class="sxs-lookup"><span data-stu-id="dfeda-125">Specifies the backup container type.</span></span>
<span data-ttu-id="dfeda-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="dfeda-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dfeda-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="dfeda-127">AzureVM</span></span>
- <span data-ttu-id="dfeda-128">Windows</span><span class="sxs-lookup"><span data-stu-id="dfeda-128">Windows</span></span>
- <span data-ttu-id="dfeda-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="dfeda-129">AzureSQL</span></span>
- <span data-ttu-id="dfeda-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="dfeda-130">AzureStorage</span></span>
- <span data-ttu-id="dfeda-131">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="dfeda-131">AzureVMAppContainer</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage, AzureVMAppContainer

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfeda-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfeda-132">-DefaultProfile</span></span>

<span data-ttu-id="dfeda-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dfeda-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfeda-134">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="dfeda-134">-FriendlyName</span></span>

<span data-ttu-id="dfeda-135">Anger namnet på den behållare som ska visas.</span><span class="sxs-lookup"><span data-stu-id="dfeda-135">Specifies the friendly name of the container to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfeda-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfeda-136">-ResourceGroupName</span></span>

<span data-ttu-id="dfeda-137">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="dfeda-137">Specifies the name of the resource group.</span></span>
<span data-ttu-id="dfeda-138">Denna parameter är endast för virtuella Azure-datorer.</span><span class="sxs-lookup"><span data-stu-id="dfeda-138">This parameter is for Azure virtual machines only.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfeda-139">-Status</span><span class="sxs-lookup"><span data-stu-id="dfeda-139">-Status</span></span>

<span data-ttu-id="dfeda-140">Anger statusen för behållar registreringen.</span><span class="sxs-lookup"><span data-stu-id="dfeda-140">Specifies the container registration status.</span></span>
<span data-ttu-id="dfeda-141">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="dfeda-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dfeda-142">Rekommendera</span><span class="sxs-lookup"><span data-stu-id="dfeda-142">Registered</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerRegistrationStatus
Parameter Sets: (All)
Aliases:
Accepted values: Registered

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfeda-143">-VaultId</span><span class="sxs-lookup"><span data-stu-id="dfeda-143">-VaultId</span></span>

<span data-ttu-id="dfeda-144">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="dfeda-144">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="dfeda-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfeda-145">CommonParameters</span></span>
<span data-ttu-id="dfeda-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfeda-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfeda-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfeda-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfeda-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dfeda-148">INPUTS</span></span>

### <span data-ttu-id="dfeda-149">System. String</span><span class="sxs-lookup"><span data-stu-id="dfeda-149">System.String</span></span>

## <span data-ttu-id="dfeda-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dfeda-150">OUTPUTS</span></span>

### <span data-ttu-id="dfeda-151">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="dfeda-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="dfeda-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dfeda-152">NOTES</span></span>

## <span data-ttu-id="dfeda-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dfeda-153">RELATED LINKS</span></span>

[<span data-ttu-id="dfeda-154">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="dfeda-154">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="dfeda-155">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="dfeda-155">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="dfeda-156">Avregistrera-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="dfeda-156">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)

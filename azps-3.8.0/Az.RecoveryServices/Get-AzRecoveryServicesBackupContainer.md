---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: c7efdf68250b0936ffd62293891eb9ebf47ad833
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088615"
---
# <span data-ttu-id="ee6da-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ee6da-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="ee6da-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ee6da-102">SYNOPSIS</span></span>

<span data-ttu-id="ee6da-103">Hämtar säkerhets kopierings behållare.</span><span class="sxs-lookup"><span data-stu-id="ee6da-103">Gets Backup containers.</span></span>

## <span data-ttu-id="ee6da-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ee6da-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee6da-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ee6da-105">DESCRIPTION</span></span>

<span data-ttu-id="ee6da-106">Cmdleten **Get-AzRecoveryServicesBackupContainer** hämtar en behållare för säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="ee6da-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="ee6da-107">En säkerhets kopia kapslar in data källor som är utformat som säkerhets kopie objekt.</span><span class="sxs-lookup"><span data-stu-id="ee6da-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="ee6da-108">Ange valv kontexten med parametern-VaultId.</span><span class="sxs-lookup"><span data-stu-id="ee6da-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="ee6da-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ee6da-109">EXAMPLES</span></span>

### <span data-ttu-id="ee6da-110">Exempel 1: Hämta en specifik behållare</span><span class="sxs-lookup"><span data-stu-id="ee6da-110">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="ee6da-111">Det här kommandot hämtar behållaren med namnet V2VM av typen AzureVM.</span><span class="sxs-lookup"><span data-stu-id="ee6da-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="ee6da-112">Exempel 2: Hämta alla behållare av en viss typ</span><span class="sxs-lookup"><span data-stu-id="ee6da-112">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="ee6da-113">Det här kommandot får alla Windows-behållare som skyddas av Azure Backup-agenten.</span><span class="sxs-lookup"><span data-stu-id="ee6da-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="ee6da-114">Parametern **BackupManagementType** krävs endast för Windows-behållare.</span><span class="sxs-lookup"><span data-stu-id="ee6da-114">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="ee6da-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ee6da-115">PARAMETERS</span></span>

### <span data-ttu-id="ee6da-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="ee6da-116">-BackupManagementType</span></span>

<span data-ttu-id="ee6da-117">Anger typen av säkerhets kopierings hantering.</span><span class="sxs-lookup"><span data-stu-id="ee6da-117">Specifies the backup management type.</span></span>
<span data-ttu-id="ee6da-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ee6da-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ee6da-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="ee6da-119">AzureVM</span></span>
- <span data-ttu-id="ee6da-120">OM</span><span class="sxs-lookup"><span data-stu-id="ee6da-120">MARS</span></span>
- <span data-ttu-id="ee6da-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="ee6da-121">AzureSQL</span></span>
- <span data-ttu-id="ee6da-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="ee6da-122">AzureStorage</span></span>

<span data-ttu-id="ee6da-123">Den här parametern används för att differentiera Windows-datorer som säkerhets kopie ras med MARS agent eller andra säkerhets kopierings motorer.</span><span class="sxs-lookup"><span data-stu-id="ee6da-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, AzureSQL, AzureStorage

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee6da-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="ee6da-124">-ContainerType</span></span>

<span data-ttu-id="ee6da-125">Anger typ av säkerhets kopierings behållare.</span><span class="sxs-lookup"><span data-stu-id="ee6da-125">Specifies the backup container type.</span></span>
<span data-ttu-id="ee6da-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ee6da-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ee6da-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="ee6da-127">AzureVM</span></span>
- <span data-ttu-id="ee6da-128">Windows</span><span class="sxs-lookup"><span data-stu-id="ee6da-128">Windows</span></span>
- <span data-ttu-id="ee6da-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="ee6da-129">AzureSQL</span></span>
- <span data-ttu-id="ee6da-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="ee6da-130">AzureStorage</span></span>
- <span data-ttu-id="ee6da-131">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="ee6da-131">AzureVMAppContainer</span></span>

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

### <span data-ttu-id="ee6da-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee6da-132">-DefaultProfile</span></span>

<span data-ttu-id="ee6da-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ee6da-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee6da-134">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ee6da-134">-FriendlyName</span></span>

<span data-ttu-id="ee6da-135">Anger namnet på den behållare som ska visas.</span><span class="sxs-lookup"><span data-stu-id="ee6da-135">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="ee6da-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee6da-136">-ResourceGroupName</span></span>

<span data-ttu-id="ee6da-137">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ee6da-137">Specifies the name of the resource group.</span></span>
<span data-ttu-id="ee6da-138">Denna parameter är endast för virtuella Azure-datorer.</span><span class="sxs-lookup"><span data-stu-id="ee6da-138">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="ee6da-139">-Status</span><span class="sxs-lookup"><span data-stu-id="ee6da-139">-Status</span></span>

<span data-ttu-id="ee6da-140">Anger statusen för behållar registreringen.</span><span class="sxs-lookup"><span data-stu-id="ee6da-140">Specifies the container registration status.</span></span>
<span data-ttu-id="ee6da-141">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ee6da-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ee6da-142">Rekommendera</span><span class="sxs-lookup"><span data-stu-id="ee6da-142">Registered</span></span>

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

### <span data-ttu-id="ee6da-143">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ee6da-143">-VaultId</span></span>

<span data-ttu-id="ee6da-144">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="ee6da-144">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ee6da-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee6da-145">CommonParameters</span></span>
<span data-ttu-id="ee6da-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee6da-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee6da-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee6da-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee6da-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ee6da-148">INPUTS</span></span>

### <span data-ttu-id="ee6da-149">System. String</span><span class="sxs-lookup"><span data-stu-id="ee6da-149">System.String</span></span>

## <span data-ttu-id="ee6da-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ee6da-150">OUTPUTS</span></span>

### <span data-ttu-id="ee6da-151">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="ee6da-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="ee6da-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ee6da-152">NOTES</span></span>

## <span data-ttu-id="ee6da-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ee6da-153">RELATED LINKS</span></span>

[<span data-ttu-id="ee6da-154">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ee6da-154">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="ee6da-155">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="ee6da-155">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="ee6da-156">Avregistrera-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ee6da-156">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)

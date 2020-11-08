---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: f061dc0f729709dee3bfe08bb22dba8d49a7f31b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100925"
---
# <span data-ttu-id="24839-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="24839-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="24839-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24839-102">SYNOPSIS</span></span>

<span data-ttu-id="24839-103">Hämtar säkerhets kopierings behållare.</span><span class="sxs-lookup"><span data-stu-id="24839-103">Gets Backup containers.</span></span>

## <span data-ttu-id="24839-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24839-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24839-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24839-105">DESCRIPTION</span></span>

<span data-ttu-id="24839-106">Cmdleten **Get-AzRecoveryServicesBackupContainer** hämtar en behållare för säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="24839-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="24839-107">En säkerhets kopia kapslar in data källor som är utformat som säkerhets kopie objekt.</span><span class="sxs-lookup"><span data-stu-id="24839-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="24839-108">Ange valv kontexten med parametern-VaultId.</span><span class="sxs-lookup"><span data-stu-id="24839-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="24839-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24839-109">EXAMPLES</span></span>

### <span data-ttu-id="24839-110">Exempel 1: Hämta en specifik behållare</span><span class="sxs-lookup"><span data-stu-id="24839-110">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="24839-111">Det här kommandot hämtar behållaren med namnet V2VM av typen AzureVM.</span><span class="sxs-lookup"><span data-stu-id="24839-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="24839-112">Exempel 2: Hämta alla behållare av en viss typ</span><span class="sxs-lookup"><span data-stu-id="24839-112">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="24839-113">Det här kommandot får alla Windows-behållare som skyddas av Azure Backup-agenten.</span><span class="sxs-lookup"><span data-stu-id="24839-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="24839-114">Parametern **BackupManagementType** krävs endast för Windows-behållare.</span><span class="sxs-lookup"><span data-stu-id="24839-114">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="24839-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24839-115">PARAMETERS</span></span>

### <span data-ttu-id="24839-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="24839-116">-BackupManagementType</span></span>

<span data-ttu-id="24839-117">Den klass med resurser som skyddas.</span><span class="sxs-lookup"><span data-stu-id="24839-117">The class of resources being protected.</span></span> <span data-ttu-id="24839-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="24839-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="24839-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="24839-119">AzureVM</span></span>
- <span data-ttu-id="24839-120">OM</span><span class="sxs-lookup"><span data-stu-id="24839-120">MARS</span></span>
- <span data-ttu-id="24839-121">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="24839-121">AzureWorkload</span></span>
- <span data-ttu-id="24839-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="24839-122">AzureStorage</span></span>

<span data-ttu-id="24839-123">Den här parametern används för att differentiera Windows-datorer som säkerhets kopie ras med MARS agent eller andra säkerhets kopierings motorer.</span><span class="sxs-lookup"><span data-stu-id="24839-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="24839-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="24839-124">-ContainerType</span></span>

<span data-ttu-id="24839-125">Anger typ av säkerhets kopierings behållare.</span><span class="sxs-lookup"><span data-stu-id="24839-125">Specifies the backup container type.</span></span>
<span data-ttu-id="24839-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="24839-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="24839-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="24839-127">AzureVM</span></span>
- <span data-ttu-id="24839-128">Windows</span><span class="sxs-lookup"><span data-stu-id="24839-128">Windows</span></span>
- <span data-ttu-id="24839-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="24839-129">AzureSQL</span></span>
- <span data-ttu-id="24839-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="24839-130">AzureStorage</span></span>
- <span data-ttu-id="24839-131">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="24839-131">AzureVMAppContainer</span></span>

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

### <span data-ttu-id="24839-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24839-132">-DefaultProfile</span></span>

<span data-ttu-id="24839-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="24839-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24839-134">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="24839-134">-FriendlyName</span></span>

<span data-ttu-id="24839-135">Anger namnet på den behållare som ska visas.</span><span class="sxs-lookup"><span data-stu-id="24839-135">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="24839-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24839-136">-ResourceGroupName</span></span>

<span data-ttu-id="24839-137">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="24839-137">Specifies the name of the resource group.</span></span>
<span data-ttu-id="24839-138">Denna parameter är endast för virtuella Azure-datorer.</span><span class="sxs-lookup"><span data-stu-id="24839-138">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="24839-139">-Status</span><span class="sxs-lookup"><span data-stu-id="24839-139">-Status</span></span>

<span data-ttu-id="24839-140">Anger statusen för behållar registreringen.</span><span class="sxs-lookup"><span data-stu-id="24839-140">Specifies the container registration status.</span></span>
<span data-ttu-id="24839-141">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="24839-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="24839-142">Rekommendera</span><span class="sxs-lookup"><span data-stu-id="24839-142">Registered</span></span>

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

### <span data-ttu-id="24839-143">-VaultId</span><span class="sxs-lookup"><span data-stu-id="24839-143">-VaultId</span></span>

<span data-ttu-id="24839-144">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="24839-144">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="24839-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24839-145">CommonParameters</span></span>
<span data-ttu-id="24839-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24839-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24839-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24839-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24839-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24839-148">INPUTS</span></span>

### <span data-ttu-id="24839-149">System. String</span><span class="sxs-lookup"><span data-stu-id="24839-149">System.String</span></span>

## <span data-ttu-id="24839-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24839-150">OUTPUTS</span></span>

### <span data-ttu-id="24839-151">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="24839-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="24839-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24839-152">NOTES</span></span>

## <span data-ttu-id="24839-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24839-153">RELATED LINKS</span></span>

[<span data-ttu-id="24839-154">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="24839-154">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="24839-155">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="24839-155">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="24839-156">Avregistrera-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="24839-156">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)
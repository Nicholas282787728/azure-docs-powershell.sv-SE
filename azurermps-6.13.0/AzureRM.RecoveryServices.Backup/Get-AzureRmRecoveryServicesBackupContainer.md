---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: c47c3e51d970302281af5a7ae3a6175f4af79739
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757047"
---
# <span data-ttu-id="f532d-101">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f532d-101">Get-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="f532d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f532d-102">SYNOPSIS</span></span>
<span data-ttu-id="f532d-103">Hämtar säkerhets kopierings behållare.</span><span class="sxs-lookup"><span data-stu-id="f532d-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f532d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f532d-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-Name] <String>] [[-FriendlyName] <String>] [[-ResourceGroupName] <String>]
 [[-Status] <ContainerRegistrationStatus>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f532d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f532d-105">DESCRIPTION</span></span>
<span data-ttu-id="f532d-106">Cmdleten **Get-AzureRmRecoveryServicesBackupContainer** hämtar en behållare för säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="f532d-106">The **Get-AzureRmRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="f532d-107">En säkerhets kopia kapslar in data källor som är utformat som säkerhets kopie objekt.</span><span class="sxs-lookup"><span data-stu-id="f532d-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="f532d-108">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f532d-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="f532d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f532d-109">EXAMPLES</span></span>

### <span data-ttu-id="f532d-110">Exempel 1: Hämta en specifik behållare</span><span class="sxs-lookup"><span data-stu-id="f532d-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="f532d-111">Det här kommandot hämtar behållaren med namnet V2VM av typen AzureVM.</span><span class="sxs-lookup"><span data-stu-id="f532d-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="f532d-112">Exempel 2: Hämta alla behållare av en viss typ</span><span class="sxs-lookup"><span data-stu-id="f532d-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="f532d-113">Det här kommandot får alla Windows-behållare som skyddas av Azure Backup-agenten.</span><span class="sxs-lookup"><span data-stu-id="f532d-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="f532d-114">Parametern *BackupManagementType* krävs endast för Windows-behållare.</span><span class="sxs-lookup"><span data-stu-id="f532d-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="f532d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f532d-115">PARAMETERS</span></span>

### <span data-ttu-id="f532d-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="f532d-116">-BackupManagementType</span></span>
<span data-ttu-id="f532d-117">Anger typen av säkerhets kopierings hantering.</span><span class="sxs-lookup"><span data-stu-id="f532d-117">Specifies the backup management type.</span></span>
<span data-ttu-id="f532d-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f532d-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f532d-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="f532d-119">AzureVM</span></span>
- <span data-ttu-id="f532d-120">OM</span><span class="sxs-lookup"><span data-stu-id="f532d-120">MARS</span></span>
- <span data-ttu-id="f532d-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="f532d-121">AzureSQL</span></span>
- <span data-ttu-id="f532d-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="f532d-122">AzureStorage</span></span>

<span data-ttu-id="f532d-123">Den här parametern används för att differentiera Windows-datorer som säkerhets kopie ras med MARS agent eller andra säkerhets kopierings motorer.</span><span class="sxs-lookup"><span data-stu-id="f532d-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="f532d-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="f532d-124">-ContainerType</span></span>
<span data-ttu-id="f532d-125">Anger typ av säkerhets kopierings behållare.</span><span class="sxs-lookup"><span data-stu-id="f532d-125">Specifies the backup container type.</span></span>
<span data-ttu-id="f532d-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f532d-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f532d-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="f532d-127">AzureVM</span></span> 
- <span data-ttu-id="f532d-128">Windows</span><span class="sxs-lookup"><span data-stu-id="f532d-128">Windows</span></span>
- <span data-ttu-id="f532d-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="f532d-129">AzureSQL</span></span>
- <span data-ttu-id="f532d-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="f532d-130">AzureStorage</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f532d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f532d-131">-DefaultProfile</span></span>
<span data-ttu-id="f532d-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f532d-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f532d-133">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f532d-133">-FriendlyName</span></span>
<span data-ttu-id="f532d-134">Anger namnet på den behållare som ska visas.</span><span class="sxs-lookup"><span data-stu-id="f532d-134">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="f532d-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="f532d-135">-Name</span></span>
<span data-ttu-id="f532d-136">Anger namnet på den behållare som ska visas.</span><span class="sxs-lookup"><span data-stu-id="f532d-136">Specifies the name of the container to get.</span></span>

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

### <span data-ttu-id="f532d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f532d-137">-ResourceGroupName</span></span>
<span data-ttu-id="f532d-138">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f532d-138">Specifies the name of the resource group.</span></span>
<span data-ttu-id="f532d-139">Denna parameter är endast för virtuella Azure-datorer.</span><span class="sxs-lookup"><span data-stu-id="f532d-139">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="f532d-140">-Status</span><span class="sxs-lookup"><span data-stu-id="f532d-140">-Status</span></span>
<span data-ttu-id="f532d-141">Anger statusen för behållar registreringen.</span><span class="sxs-lookup"><span data-stu-id="f532d-141">Specifies the container registration status.</span></span>
<span data-ttu-id="f532d-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f532d-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f532d-143">Rekommendera</span><span class="sxs-lookup"><span data-stu-id="f532d-143">Registered</span></span>

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

### <span data-ttu-id="f532d-144">-VaultId</span><span class="sxs-lookup"><span data-stu-id="f532d-144">-VaultId</span></span>
<span data-ttu-id="f532d-145">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="f532d-145">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f532d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f532d-146">CommonParameters</span></span>
<span data-ttu-id="f532d-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f532d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f532d-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f532d-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f532d-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f532d-149">INPUTS</span></span>

### <span data-ttu-id="f532d-150">System. String</span><span class="sxs-lookup"><span data-stu-id="f532d-150">System.String</span></span>
<span data-ttu-id="f532d-151">Parametrar: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f532d-151">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="f532d-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f532d-152">OUTPUTS</span></span>

### <span data-ttu-id="f532d-153">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="f532d-153">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="f532d-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f532d-154">NOTES</span></span>

## <span data-ttu-id="f532d-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f532d-155">RELATED LINKS</span></span>

[<span data-ttu-id="f532d-156">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="f532d-156">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="f532d-157">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="f532d-157">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="f532d-158">Avregistrera-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f532d-158">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>](./Unregister-AzureRmRecoveryServicesBackupContainer.md)



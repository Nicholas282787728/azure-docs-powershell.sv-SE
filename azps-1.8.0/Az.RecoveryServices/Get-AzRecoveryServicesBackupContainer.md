---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 73438a3f294aaece7c4649f53559311d95ef4aa0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747440"
---
# <span data-ttu-id="658cf-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="658cf-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="658cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="658cf-102">SYNOPSIS</span></span>
<span data-ttu-id="658cf-103">Hämtar säkerhets kopierings behållare.</span><span class="sxs-lookup"><span data-stu-id="658cf-103">Gets Backup containers.</span></span>

## <span data-ttu-id="658cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="658cf-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="658cf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="658cf-105">DESCRIPTION</span></span>
<span data-ttu-id="658cf-106">Cmdleten **Get-AzRecoveryServicesBackupContainer** hämtar en behållare för säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="658cf-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="658cf-107">En säkerhets kopia kapslar in data källor som är utformat som säkerhets kopie objekt.</span><span class="sxs-lookup"><span data-stu-id="658cf-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="658cf-108">Ställ in valv kontexten med hjälp av Set-AzRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="658cf-108">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="658cf-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="658cf-109">EXAMPLES</span></span>

### <span data-ttu-id="658cf-110">Exempel 1: Hämta en specifik behållare</span><span class="sxs-lookup"><span data-stu-id="658cf-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="658cf-111">Det här kommandot hämtar behållaren med namnet V2VM av typen AzureVM.</span><span class="sxs-lookup"><span data-stu-id="658cf-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="658cf-112">Exempel 2: Hämta alla behållare av en viss typ</span><span class="sxs-lookup"><span data-stu-id="658cf-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="658cf-113">Det här kommandot får alla Windows-behållare som skyddas av Azure Backup-agenten.</span><span class="sxs-lookup"><span data-stu-id="658cf-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="658cf-114">Parametern *BackupManagementType* krävs endast för Windows-behållare.</span><span class="sxs-lookup"><span data-stu-id="658cf-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="658cf-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="658cf-115">PARAMETERS</span></span>

### <span data-ttu-id="658cf-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="658cf-116">-BackupManagementType</span></span>
<span data-ttu-id="658cf-117">Anger typen av säkerhets kopierings hantering.</span><span class="sxs-lookup"><span data-stu-id="658cf-117">Specifies the backup management type.</span></span>
<span data-ttu-id="658cf-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="658cf-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="658cf-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="658cf-119">AzureVM</span></span>
- <span data-ttu-id="658cf-120">OM</span><span class="sxs-lookup"><span data-stu-id="658cf-120">MARS</span></span>
- <span data-ttu-id="658cf-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="658cf-121">AzureSQL</span></span>
- <span data-ttu-id="658cf-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="658cf-122">AzureStorage</span></span>

<span data-ttu-id="658cf-123">Den här parametern används för att differentiera Windows-datorer som säkerhets kopie ras med MARS agent eller andra säkerhets kopierings motorer.</span><span class="sxs-lookup"><span data-stu-id="658cf-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="658cf-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="658cf-124">-ContainerType</span></span>
<span data-ttu-id="658cf-125">Anger typ av säkerhets kopierings behållare.</span><span class="sxs-lookup"><span data-stu-id="658cf-125">Specifies the backup container type.</span></span>
<span data-ttu-id="658cf-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="658cf-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="658cf-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="658cf-127">AzureVM</span></span> 
- <span data-ttu-id="658cf-128">Windows</span><span class="sxs-lookup"><span data-stu-id="658cf-128">Windows</span></span>
- <span data-ttu-id="658cf-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="658cf-129">AzureSQL</span></span>
- <span data-ttu-id="658cf-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="658cf-130">AzureStorage</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="658cf-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="658cf-131">-DefaultProfile</span></span>
<span data-ttu-id="658cf-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="658cf-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="658cf-133">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="658cf-133">-FriendlyName</span></span>
<span data-ttu-id="658cf-134">Anger namnet på den behållare som ska visas.</span><span class="sxs-lookup"><span data-stu-id="658cf-134">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="658cf-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="658cf-135">-ResourceGroupName</span></span>
<span data-ttu-id="658cf-136">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="658cf-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="658cf-137">Denna parameter är endast för virtuella Azure-datorer.</span><span class="sxs-lookup"><span data-stu-id="658cf-137">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="658cf-138">-Status</span><span class="sxs-lookup"><span data-stu-id="658cf-138">-Status</span></span>
<span data-ttu-id="658cf-139">Anger statusen för behållar registreringen.</span><span class="sxs-lookup"><span data-stu-id="658cf-139">Specifies the container registration status.</span></span>
<span data-ttu-id="658cf-140">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="658cf-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="658cf-141">Rekommendera</span><span class="sxs-lookup"><span data-stu-id="658cf-141">Registered</span></span>

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

### <span data-ttu-id="658cf-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="658cf-142">-VaultId</span></span>
<span data-ttu-id="658cf-143">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="658cf-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="658cf-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="658cf-144">CommonParameters</span></span>
<span data-ttu-id="658cf-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="658cf-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="658cf-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="658cf-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="658cf-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="658cf-147">INPUTS</span></span>

### <span data-ttu-id="658cf-148">System. String</span><span class="sxs-lookup"><span data-stu-id="658cf-148">System.String</span></span>

## <span data-ttu-id="658cf-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="658cf-149">OUTPUTS</span></span>

### <span data-ttu-id="658cf-150">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="658cf-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="658cf-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="658cf-151">NOTES</span></span>

## <span data-ttu-id="658cf-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="658cf-152">RELATED LINKS</span></span>

[<span data-ttu-id="658cf-153">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="658cf-153">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="658cf-154">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="658cf-154">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="658cf-155">Avregistrera-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="658cf-155">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)


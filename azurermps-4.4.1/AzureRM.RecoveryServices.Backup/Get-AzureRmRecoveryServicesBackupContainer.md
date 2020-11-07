---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: e6b0633b43bc93c516c9c5b6f4872ecbd6d68520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757765"
---
# <span data-ttu-id="3d9c9-101">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="3d9c9-101">Get-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="3d9c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d9c9-102">SYNOPSIS</span></span>
<span data-ttu-id="3d9c9-103">Hämtar säkerhets kopierings behållare.</span><span class="sxs-lookup"><span data-stu-id="3d9c9-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d9c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d9c9-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-Name] <String>] [[-FriendlyName] <String>] [[-ResourceGroupName] <String>]
 [[-Status] <ContainerRegistrationStatus>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d9c9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d9c9-105">DESCRIPTION</span></span>
<span data-ttu-id="3d9c9-106">Cmdleten **Get-AzureRmRecoveryServicesBackupContainer** hämtar en behållare för säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="3d9c9-106">The **Get-AzureRmRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="3d9c9-107">En säkerhets kopia kapslar in data källor som är utformat som säkerhets kopie objekt.</span><span class="sxs-lookup"><span data-stu-id="3d9c9-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>

<span data-ttu-id="3d9c9-108">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d9c9-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="3d9c9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d9c9-109">EXAMPLES</span></span>

### <span data-ttu-id="3d9c9-110">Exempel 1: Hämta en specifik behållare</span><span class="sxs-lookup"><span data-stu-id="3d9c9-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="3d9c9-111">Det här kommandot hämtar behållaren med namnet V2VM av typen AzureVM.</span><span class="sxs-lookup"><span data-stu-id="3d9c9-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="3d9c9-112">Exempel 2: Hämta alla behållare av en viss typ</span><span class="sxs-lookup"><span data-stu-id="3d9c9-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="3d9c9-113">Det här kommandot får alla Windows-behållare som skyddas av Azure Backup-agenten.</span><span class="sxs-lookup"><span data-stu-id="3d9c9-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="3d9c9-114">Parametern *BackupManagementType* krävs endast för Windows-behållare.</span><span class="sxs-lookup"><span data-stu-id="3d9c9-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="3d9c9-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d9c9-115">PARAMETERS</span></span>

### <span data-ttu-id="3d9c9-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="3d9c9-116">-BackupManagementType</span></span>
<span data-ttu-id="3d9c9-117">Anger typen av säkerhets kopierings hantering.</span><span class="sxs-lookup"><span data-stu-id="3d9c9-117">Specifies the backup management type.</span></span>
<span data-ttu-id="3d9c9-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3d9c9-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3d9c9-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="3d9c9-119">AzureVM</span></span>
- <span data-ttu-id="3d9c9-120">OM</span><span class="sxs-lookup"><span data-stu-id="3d9c9-120">MARS</span></span>
- <span data-ttu-id="3d9c9-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="3d9c9-121">AzureSQL</span></span>

<span data-ttu-id="3d9c9-122">Den här parametern används för att differentiera Windows-datorer som säkerhets kopie ras med MARS agent eller andra säkerhets kopierings motorer.</span><span class="sxs-lookup"><span data-stu-id="3d9c9-122">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, AzureSQL

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d9c9-123">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="3d9c9-123">-ContainerType</span></span>
<span data-ttu-id="3d9c9-124">Anger typ av säkerhets kopierings behållare.</span><span class="sxs-lookup"><span data-stu-id="3d9c9-124">Specifies the backup container type.</span></span>
<span data-ttu-id="3d9c9-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3d9c9-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3d9c9-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="3d9c9-126">AzureVM</span></span> 
- <span data-ttu-id="3d9c9-127">Windows</span><span class="sxs-lookup"><span data-stu-id="3d9c9-127">Windows</span></span>
- <span data-ttu-id="3d9c9-128">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="3d9c9-128">AzureSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, Windows, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d9c9-129">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3d9c9-129">-FriendlyName</span></span>
<span data-ttu-id="3d9c9-130">Anger namnet på den behållare som ska visas.</span><span class="sxs-lookup"><span data-stu-id="3d9c9-130">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="3d9c9-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="3d9c9-131">-Name</span></span>
<span data-ttu-id="3d9c9-132">Anger namnet på den behållare som ska visas.</span><span class="sxs-lookup"><span data-stu-id="3d9c9-132">Specifies the name of the container to get.</span></span>

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

### <span data-ttu-id="3d9c9-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d9c9-133">-ResourceGroupName</span></span>
<span data-ttu-id="3d9c9-134">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3d9c9-134">Specifies the name of the resource group.</span></span>
<span data-ttu-id="3d9c9-135">Denna parameter är endast för virtuella Azure-datorer.</span><span class="sxs-lookup"><span data-stu-id="3d9c9-135">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="3d9c9-136">-Status</span><span class="sxs-lookup"><span data-stu-id="3d9c9-136">-Status</span></span>
<span data-ttu-id="3d9c9-137">Anger statusen för behållar registreringen.</span><span class="sxs-lookup"><span data-stu-id="3d9c9-137">Specifies the container registration status.</span></span>
<span data-ttu-id="3d9c9-138">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3d9c9-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3d9c9-139">Rekommendera</span><span class="sxs-lookup"><span data-stu-id="3d9c9-139">Registered</span></span>

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

### <span data-ttu-id="3d9c9-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d9c9-140">-DefaultProfile</span></span>
<span data-ttu-id="3d9c9-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d9c9-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d9c9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d9c9-142">CommonParameters</span></span>
<span data-ttu-id="3d9c9-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d9c9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d9c9-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d9c9-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d9c9-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d9c9-145">INPUTS</span></span>

## <span data-ttu-id="3d9c9-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d9c9-146">OUTPUTS</span></span>

### <span data-ttu-id="3d9c9-147">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="3d9c9-147">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="3d9c9-148">System. Collections. Generic. IList ' 1 [Microsoft. Azure. kommandon. RecoveryServices. backup. cmdletar. MODELES. ContainerBase]</span><span class="sxs-lookup"><span data-stu-id="3d9c9-148">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase]</span></span>

## <span data-ttu-id="3d9c9-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d9c9-149">NOTES</span></span>

## <span data-ttu-id="3d9c9-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d9c9-150">RELATED LINKS</span></span>

[<span data-ttu-id="3d9c9-151">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3d9c9-151">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="3d9c9-152">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="3d9c9-152">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="3d9c9-153">Avregistrera-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="3d9c9-153">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>](./Unregister-AzureRmRecoveryServicesBackupContainer.md)



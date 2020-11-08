---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 293cd11c146369644ca67ba76158c251b1480d22
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092462"
---
# <span data-ttu-id="79fff-101">Get-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="79fff-101">Get-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="79fff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79fff-102">SYNOPSIS</span></span>
<span data-ttu-id="79fff-103">Med det här kommandot hämtas alla skydds bara objekt i en viss behållare eller i alla registrerade behållare.</span><span class="sxs-lookup"><span data-stu-id="79fff-103">This command will retrieve all protectable items within a certain container or across all registered containers.</span></span> <span data-ttu-id="79fff-104">Det består av alla element i programmets hierarki.</span><span class="sxs-lookup"><span data-stu-id="79fff-104">It will consist of all the elements of the hierarchy of the application.</span></span> <span data-ttu-id="79fff-105">Returnerar DBs och deras övre nivå enheter som förekomst, AvailabilityGroup osv.</span><span class="sxs-lookup"><span data-stu-id="79fff-105">Returns DBs and their upper tier entities like Instance, AvailabilityGroup etc.</span></span>

## <span data-ttu-id="79fff-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79fff-106">SYNTAX</span></span>

### <span data-ttu-id="79fff-107">NoFilterParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="79fff-107">NoFilterParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79fff-108">FilterParamSet</span><span class="sxs-lookup"><span data-stu-id="79fff-108">FilterParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [[-ItemType] <ProtectableItemType>] [-Name <String>] [-ServerName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79fff-109">IdParamSet</span><span class="sxs-lookup"><span data-stu-id="79fff-109">IdParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [-ParentID] <String> [[-ItemType] <ProtectableItemType>]
 [-Name <String>] [-ServerName <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79fff-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79fff-110">DESCRIPTION</span></span>
<span data-ttu-id="79fff-111">Cmdleten **Get-AzRecoveryServicesBackupProtectableItem** hämtar de skyddade objekten i en behållare eller ett värde i Azure Backup och objektets skydds status.</span><span class="sxs-lookup"><span data-stu-id="79fff-111">The **Get-AzRecoveryServicesBackupProtectableItem** cmdlet gets the protectable items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="79fff-112">En behållare som är registrerad på ett Azure Recovery Services-valv kan ha en eller flera objekt som kan skyddas.</span><span class="sxs-lookup"><span data-stu-id="79fff-112">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>

## <span data-ttu-id="79fff-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79fff-113">EXAMPLES</span></span>

### <span data-ttu-id="79fff-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="79fff-114">Example 1</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType MSSQL -Status Registered
PS C:\> $Item = Get-AzRecoveryServicesProtectableItem -Container $Container -ItemType "SQLDatabase" -VaultId $vault.ID
```

<span data-ttu-id="79fff-115">Det första kommandot får behållaren av typen MSSQL och lagrar den sedan i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="79fff-115">The first command gets the container of type MSSQL, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="79fff-116">Det andra kommandot får säkerhets kopian i $Container och lagrar det sedan i $Item-variabeln.</span><span class="sxs-lookup"><span data-stu-id="79fff-116">The second command gets the Backup item in $Container, and then stores it in the $Item variable.</span></span>

## <span data-ttu-id="79fff-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79fff-117">PARAMETERS</span></span>

### <span data-ttu-id="79fff-118">-Container</span><span class="sxs-lookup"><span data-stu-id="79fff-118">-Container</span></span>
<span data-ttu-id="79fff-119">Behållare där objektet finns</span><span class="sxs-lookup"><span data-stu-id="79fff-119">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79fff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79fff-120">-DefaultProfile</span></span>
<span data-ttu-id="79fff-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="79fff-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79fff-122">-ItemType</span><span class="sxs-lookup"><span data-stu-id="79fff-122">-ItemType</span></span>
<span data-ttu-id="79fff-123">Anger typen av objekt som skyddas.</span><span class="sxs-lookup"><span data-stu-id="79fff-123">Specifies the type of protectable item.</span></span> <span data-ttu-id="79fff-124">Tillämpliga värden: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span><span class="sxs-lookup"><span data-stu-id="79fff-124">Applicable values: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemType
Parameter Sets: FilterParamSet, IdParamSet
Aliases:
Accepted values: SQLDataBase, SQLInstance, SQLAvailabilityGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fff-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="79fff-125">-Name</span></span>
<span data-ttu-id="79fff-126">Anger namnet på databasen, instansen eller AvailabilityGroup.</span><span class="sxs-lookup"><span data-stu-id="79fff-126">Specifies the name of the Database, Instance or AvailabilityGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterParamSet, IdParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fff-127">-</span><span class="sxs-lookup"><span data-stu-id="79fff-127">-ParentID</span></span>
<span data-ttu-id="79fff-128">Ange ARM-ID för en instans eller AG.</span><span class="sxs-lookup"><span data-stu-id="79fff-128">Specified the ARM ID of an Instance or AG.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79fff-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="79fff-129">-ServerName</span></span>
<span data-ttu-id="79fff-130">Anger namnet på den server som objektet tillhör.</span><span class="sxs-lookup"><span data-stu-id="79fff-130">Specifies the name of the server to which the item belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterParamSet, IdParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fff-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="79fff-131">-VaultId</span></span>
<span data-ttu-id="79fff-132">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="79fff-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="79fff-133">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="79fff-133">-WorkloadType</span></span>
<span data-ttu-id="79fff-134">Resursens arbets typ (till exempel: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="79fff-134">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fff-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79fff-135">CommonParameters</span></span>
<span data-ttu-id="79fff-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79fff-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79fff-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79fff-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79fff-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79fff-138">INPUTS</span></span>

### <span data-ttu-id="79fff-139">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="79fff-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="79fff-140">System. String</span><span class="sxs-lookup"><span data-stu-id="79fff-140">System.String</span></span>

## <span data-ttu-id="79fff-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79fff-141">OUTPUTS</span></span>

### <span data-ttu-id="79fff-142">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ProtectableItemBase</span><span class="sxs-lookup"><span data-stu-id="79fff-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span></span>

## <span data-ttu-id="79fff-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79fff-143">NOTES</span></span>

## <span data-ttu-id="79fff-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79fff-144">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: add399ca208cdcd1f1b4395523f8df43875ff451
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271714"
---
# <span data-ttu-id="bb09a-101">Get-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="bb09a-101">Get-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="bb09a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bb09a-102">SYNOPSIS</span></span>
<span data-ttu-id="bb09a-103">Med det här kommandot hämtas alla skydds bara objekt i en viss behållare eller i alla registrerade behållare.</span><span class="sxs-lookup"><span data-stu-id="bb09a-103">This command will retrieve all protectable items within a certain container or across all registered containers.</span></span> <span data-ttu-id="bb09a-104">Det består av alla element i programmets hierarki.</span><span class="sxs-lookup"><span data-stu-id="bb09a-104">It will consist of all the elements of the hierarchy of the application.</span></span> <span data-ttu-id="bb09a-105">Returnerar DBs och deras övre nivå enheter som förekomst, AvailabilityGroup osv.</span><span class="sxs-lookup"><span data-stu-id="bb09a-105">Returns DBs and their upper tier entities like Instance, AvailabilityGroup etc.</span></span>

## <span data-ttu-id="bb09a-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bb09a-106">SYNTAX</span></span>

### <span data-ttu-id="bb09a-107">NoFilterParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="bb09a-107">NoFilterParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb09a-108">FilterParamSet</span><span class="sxs-lookup"><span data-stu-id="bb09a-108">FilterParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [[-ItemType] <ProtectableItemType>] [-Name <String>] [-ServerName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb09a-109">IdParamSet</span><span class="sxs-lookup"><span data-stu-id="bb09a-109">IdParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [-ParentID] <String> [[-ItemType] <ProtectableItemType>]
 [-Name <String>] [-ServerName <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb09a-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bb09a-110">DESCRIPTION</span></span>
<span data-ttu-id="bb09a-111">Cmdleten **Get-AzRecoveryServicesBackupProtectableItem** hämtar listan över objekt som skyddas i en behållare och objektets skydds status.</span><span class="sxs-lookup"><span data-stu-id="bb09a-111">The **Get-AzRecoveryServicesBackupProtectableItem** cmdlet gets the list of protectable items in a container and the protection status of the items.</span></span>
<span data-ttu-id="bb09a-112">En behållare som är registrerad på ett Azure Recovery Services-valv kan ha en eller flera objekt som kan skyddas.</span><span class="sxs-lookup"><span data-stu-id="bb09a-112">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>

## <span data-ttu-id="bb09a-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bb09a-113">EXAMPLES</span></span>

### <span data-ttu-id="bb09a-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bb09a-114">Example 1</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType MSSQL -Status Registered
PS C:\> $Item = Get-AzRecoveryServicesProtectableItem -Container $Container -ItemType "SQLDatabase" -VaultId $vault.ID
```

<span data-ttu-id="bb09a-115">Det första kommandot får behållaren av typen MSSQL och lagrar den sedan i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="bb09a-115">The first command gets the container of type MSSQL, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="bb09a-116">Det andra kommandot skyddar det skyddade objektet för säkerhets kopiering i $Container och lagrar det sedan i $Item-variabeln.</span><span class="sxs-lookup"><span data-stu-id="bb09a-116">The second command gets the Backup protectable item in $Container, and then stores it in the $Item variable.</span></span>

## <span data-ttu-id="bb09a-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bb09a-117">PARAMETERS</span></span>

### <span data-ttu-id="bb09a-118">-Container</span><span class="sxs-lookup"><span data-stu-id="bb09a-118">-Container</span></span>
<span data-ttu-id="bb09a-119">Behållare där objektet finns</span><span class="sxs-lookup"><span data-stu-id="bb09a-119">Container where the item resides</span></span>

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

### <span data-ttu-id="bb09a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb09a-120">-DefaultProfile</span></span>
<span data-ttu-id="bb09a-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bb09a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb09a-122">-ItemType</span><span class="sxs-lookup"><span data-stu-id="bb09a-122">-ItemType</span></span>
<span data-ttu-id="bb09a-123">Anger typen av objekt som skyddas.</span><span class="sxs-lookup"><span data-stu-id="bb09a-123">Specifies the type of protectable item.</span></span> <span data-ttu-id="bb09a-124">Tillämpliga värden: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span><span class="sxs-lookup"><span data-stu-id="bb09a-124">Applicable values: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span></span>

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

### <span data-ttu-id="bb09a-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="bb09a-125">-Name</span></span>
<span data-ttu-id="bb09a-126">Anger namnet på databasen, instansen eller AvailabilityGroup.</span><span class="sxs-lookup"><span data-stu-id="bb09a-126">Specifies the name of the Database, Instance or AvailabilityGroup.</span></span>

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

### <span data-ttu-id="bb09a-127">-</span><span class="sxs-lookup"><span data-stu-id="bb09a-127">-ParentID</span></span>
<span data-ttu-id="bb09a-128">Ange ARM-ID för en instans eller AG.</span><span class="sxs-lookup"><span data-stu-id="bb09a-128">Specified the ARM ID of an Instance or AG.</span></span>

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

### <span data-ttu-id="bb09a-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bb09a-129">-ServerName</span></span>
<span data-ttu-id="bb09a-130">Anger namnet på den server som objektet tillhör.</span><span class="sxs-lookup"><span data-stu-id="bb09a-130">Specifies the name of the server to which the item belongs.</span></span>

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

### <span data-ttu-id="bb09a-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="bb09a-131">-VaultId</span></span>
<span data-ttu-id="bb09a-132">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="bb09a-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="bb09a-133">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="bb09a-133">-WorkloadType</span></span>
<span data-ttu-id="bb09a-134">Arbets belastnings typ för resursen.</span><span class="sxs-lookup"><span data-stu-id="bb09a-134">Workload type of the resource.</span></span> <span data-ttu-id="bb09a-135">De aktuella värdena är AzureVM, WindowsServer, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="bb09a-135">The current supported values are  AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:
Accepted values: AzureVM, WindowsServer, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb09a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb09a-136">CommonParameters</span></span>
<span data-ttu-id="bb09a-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb09a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb09a-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb09a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb09a-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bb09a-139">INPUTS</span></span>

### <span data-ttu-id="bb09a-140">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="bb09a-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="bb09a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bb09a-141">System.String</span></span>

## <span data-ttu-id="bb09a-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bb09a-142">OUTPUTS</span></span>

### <span data-ttu-id="bb09a-143">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ProtectableItemBase</span><span class="sxs-lookup"><span data-stu-id="bb09a-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span></span>

## <span data-ttu-id="bb09a-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bb09a-144">NOTES</span></span>

## <span data-ttu-id="bb09a-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bb09a-145">RELATED LINKS</span></span>

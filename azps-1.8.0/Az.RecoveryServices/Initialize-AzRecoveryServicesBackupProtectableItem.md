---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/initialize-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 0fd0473cccdf8fbef3d3bab941ab6b3ce7813a63
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747403"
---
# <span data-ttu-id="8fa3d-101">Initialize-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="8fa3d-101">Initialize-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="8fa3d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8fa3d-102">SYNOPSIS</span></span>
<span data-ttu-id="8fa3d-103">Det här kommandot utlöser identifieringen av oskyddade objekt av den angivna typen av arbets belastning i den angivna behållaren.</span><span class="sxs-lookup"><span data-stu-id="8fa3d-103">This command triggers the discovery of any unprotected items of the given workload type in the given container.</span></span> <span data-ttu-id="8fa3d-104">Om DB-programmet inte är skyddat automatiskt använder du det här kommandot för att identifiera nya DBs när de läggs till och fortsätter för att skydda dem.</span><span class="sxs-lookup"><span data-stu-id="8fa3d-104">If the DB application is not auto-protected use this command to discover new DBs whenever they are added and proceed to protect them.</span></span>

## <span data-ttu-id="8fa3d-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8fa3d-105">SYNTAX</span></span>

```
Initialize-AzRecoveryServicesBackupProtectableItem [-Container] <ContainerBase> [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fa3d-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8fa3d-106">DESCRIPTION</span></span>
<span data-ttu-id="8fa3d-107">cmdleten söker efter specifika arbets belastningar i en behållare.</span><span class="sxs-lookup"><span data-stu-id="8fa3d-107">the cmdlet enquires for specific workloads within a container.</span></span> <span data-ttu-id="8fa3d-108">Då utlöses en åtgärd som skapar skyddade objekt.</span><span class="sxs-lookup"><span data-stu-id="8fa3d-108">This triggers an operation which creates protectable items.</span></span>

## <span data-ttu-id="8fa3d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8fa3d-109">EXAMPLES</span></span>

### <span data-ttu-id="8fa3d-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8fa3d-110">Example 1</span></span>
```
PS C:\> Initialize-AzRecoveryServicesProtectableItem -Container $Container –WorkloadType “MSSQL”
```

<span data-ttu-id="8fa3d-111">Cmdleten kör en identifierings åtgärd för nya oskyddade objekt.</span><span class="sxs-lookup"><span data-stu-id="8fa3d-111">The cmdlet executes a discovery operation for new protectable items.</span></span>

## <span data-ttu-id="8fa3d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8fa3d-112">PARAMETERS</span></span>

### <span data-ttu-id="8fa3d-113">-Container</span><span class="sxs-lookup"><span data-stu-id="8fa3d-113">-Container</span></span>
<span data-ttu-id="8fa3d-114">Behållare där objektet finns</span><span class="sxs-lookup"><span data-stu-id="8fa3d-114">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa3d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fa3d-115">-DefaultProfile</span></span>
<span data-ttu-id="8fa3d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8fa3d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fa3d-117">-VaultId</span><span class="sxs-lookup"><span data-stu-id="8fa3d-117">-VaultId</span></span>
<span data-ttu-id="8fa3d-118">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="8fa3d-118">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8fa3d-119">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="8fa3d-119">-WorkloadType</span></span>
<span data-ttu-id="8fa3d-120">Resursens arbets typ (till exempel: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="8fa3d-120">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fa3d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fa3d-121">CommonParameters</span></span>
<span data-ttu-id="8fa3d-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fa3d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fa3d-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fa3d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fa3d-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8fa3d-124">INPUTS</span></span>

### <span data-ttu-id="8fa3d-125">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="8fa3d-125">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="8fa3d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8fa3d-126">System.String</span></span>

## <span data-ttu-id="8fa3d-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8fa3d-127">OUTPUTS</span></span>

### <span data-ttu-id="8fa3d-128">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="8fa3d-128">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="8fa3d-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8fa3d-129">NOTES</span></span>

## <span data-ttu-id="8fa3d-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8fa3d-130">RELATED LINKS</span></span>
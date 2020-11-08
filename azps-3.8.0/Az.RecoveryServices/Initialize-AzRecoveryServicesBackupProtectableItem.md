---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/initialize-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 8bc2286cf6df736ee54390447e83f0337c031001
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092434"
---
# <span data-ttu-id="fe36e-101">Initialize-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="fe36e-101">Initialize-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="fe36e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe36e-102">SYNOPSIS</span></span>
<span data-ttu-id="fe36e-103">Det här kommandot utlöser identifieringen av oskyddade objekt av den angivna typen av arbets belastning i den angivna behållaren.</span><span class="sxs-lookup"><span data-stu-id="fe36e-103">This command triggers the discovery of any unprotected items of the given workload type in the given container.</span></span> <span data-ttu-id="fe36e-104">Om DB-programmet inte är skyddat automatiskt använder du det här kommandot för att identifiera nya DBs när de läggs till och fortsätter för att skydda dem.</span><span class="sxs-lookup"><span data-stu-id="fe36e-104">If the DB application is not auto-protected use this command to discover new DBs whenever they are added and proceed to protect them.</span></span>

## <span data-ttu-id="fe36e-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe36e-105">SYNTAX</span></span>

```
Initialize-AzRecoveryServicesBackupProtectableItem [-Container] <ContainerBase> [-WorkloadType] <WorkloadType>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe36e-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe36e-106">DESCRIPTION</span></span>
<span data-ttu-id="fe36e-107">cmdleten söker efter specifika arbets belastningar i en behållare.</span><span class="sxs-lookup"><span data-stu-id="fe36e-107">the cmdlet enquires for specific workloads within a container.</span></span> <span data-ttu-id="fe36e-108">Då utlöses en åtgärd som skapar skyddade objekt.</span><span class="sxs-lookup"><span data-stu-id="fe36e-108">This triggers an operation which creates protectable items.</span></span>

## <span data-ttu-id="fe36e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe36e-109">EXAMPLES</span></span>

### <span data-ttu-id="fe36e-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fe36e-110">Example 1</span></span>
```
PS C:\> Initialize-AzRecoveryServicesProtectableItem -Container $Container -WorkloadType "MSSQL"
```

<span data-ttu-id="fe36e-111">Cmdleten kör en identifierings åtgärd för nya oskyddade objekt.</span><span class="sxs-lookup"><span data-stu-id="fe36e-111">The cmdlet executes a discovery operation for new protectable items.</span></span>

## <span data-ttu-id="fe36e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe36e-112">PARAMETERS</span></span>

### <span data-ttu-id="fe36e-113">-Container</span><span class="sxs-lookup"><span data-stu-id="fe36e-113">-Container</span></span>
<span data-ttu-id="fe36e-114">Behållare där objektet finns</span><span class="sxs-lookup"><span data-stu-id="fe36e-114">Container where the item resides</span></span>

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

### <span data-ttu-id="fe36e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe36e-115">-DefaultProfile</span></span>
<span data-ttu-id="fe36e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fe36e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe36e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe36e-117">-PassThru</span></span>
<span data-ttu-id="fe36e-118">Returnera behållaren som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="fe36e-118">Return the container to be deleted.</span></span>

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

### <span data-ttu-id="fe36e-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="fe36e-119">-VaultId</span></span>
<span data-ttu-id="fe36e-120">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="fe36e-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="fe36e-121">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="fe36e-121">-WorkloadType</span></span>
<span data-ttu-id="fe36e-122">Resursens arbets typ (till exempel: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="fe36e-122">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

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

### <span data-ttu-id="fe36e-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fe36e-123">-Confirm</span></span>
<span data-ttu-id="fe36e-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fe36e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe36e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe36e-125">-WhatIf</span></span>
<span data-ttu-id="fe36e-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fe36e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe36e-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fe36e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe36e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe36e-128">CommonParameters</span></span>
<span data-ttu-id="fe36e-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe36e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe36e-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe36e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe36e-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe36e-131">INPUTS</span></span>

### <span data-ttu-id="fe36e-132">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="fe36e-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="fe36e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fe36e-133">System.String</span></span>

## <span data-ttu-id="fe36e-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe36e-134">OUTPUTS</span></span>

### <span data-ttu-id="fe36e-135">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="fe36e-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="fe36e-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe36e-136">NOTES</span></span>

## <span data-ttu-id="fe36e-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe36e-137">RELATED LINKS</span></span>

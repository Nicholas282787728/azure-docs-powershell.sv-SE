---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 5452758a5cf269ef50475b8962e5fbca117dbb1d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920166"
---
# <span data-ttu-id="103e6-101">Unregister-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="103e6-101">Unregister-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="103e6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="103e6-102">SYNOPSIS</span></span>
<span data-ttu-id="103e6-103">Avregistrerar en SCDPM-Server eller reserv Server från valvet.</span><span class="sxs-lookup"><span data-stu-id="103e6-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

## <span data-ttu-id="103e6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="103e6-104">SYNTAX</span></span>

```
Unregister-AzRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="103e6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="103e6-105">DESCRIPTION</span></span>
<span data-ttu-id="103e6-106">Med cmdleten **Unregistered-AzRecoveryServicesBackupManagementServer** avregistrerar du en System Center Data Protection Manager-Server (SCDPM) eller en Azure Backup-Server från valvet.</span><span class="sxs-lookup"><span data-stu-id="103e6-106">The **Unregister-AzRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="103e6-107">Denna cmdlet tar bort referenser till de servrar som avregistrerats från valvet.</span><span class="sxs-lookup"><span data-stu-id="103e6-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>
<span data-ttu-id="103e6-108">Innan du kan avregistrera en behållare måste du ta bort alla skyddade data som är kopplade till den behållaren.</span><span class="sxs-lookup"><span data-stu-id="103e6-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="103e6-109">Ställ in valv kontexten med hjälp av Set-AzRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="103e6-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="103e6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="103e6-110">EXAMPLES</span></span>

### <span data-ttu-id="103e6-111">Exempel 1: avregistrera en SCDPM-Server från valvet</span><span class="sxs-lookup"><span data-stu-id="103e6-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```
PS C:\>$BMS = Get-AzRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupManagementServer -AzBackupManagementServer $BMS
```

<span data-ttu-id="103e6-112">Det första kommandot får säkerhets kopierings servern med namnet dpmserver01.contoso.com och lagrar den sedan i $BMS variabel.</span><span class="sxs-lookup"><span data-stu-id="103e6-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>
<span data-ttu-id="103e6-113">Det andra kommandot avregistrerar SCDPM-servern från valvet.</span><span class="sxs-lookup"><span data-stu-id="103e6-113">The second command unregisters the SCDPM server from the vault.</span></span>

## <span data-ttu-id="103e6-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="103e6-114">PARAMETERS</span></span>

### <span data-ttu-id="103e6-115">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="103e6-115">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="103e6-116">Behållare för säkerhets kopiering av återställnings tjänster.</span><span class="sxs-lookup"><span data-stu-id="103e6-116">The recovery services backup container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="103e6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="103e6-117">-DefaultProfile</span></span>
<span data-ttu-id="103e6-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="103e6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="103e6-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="103e6-119">-PassThru</span></span>
<span data-ttu-id="103e6-120">Returnera säkerhets kopierings hanterings servern som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="103e6-120">Return the Backup Management Server to be deleted.</span></span>

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

### <span data-ttu-id="103e6-121">-VaultId</span><span class="sxs-lookup"><span data-stu-id="103e6-121">-VaultId</span></span>
<span data-ttu-id="103e6-122">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="103e6-122">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="103e6-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="103e6-123">-Confirm</span></span>
<span data-ttu-id="103e6-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="103e6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="103e6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="103e6-125">-WhatIf</span></span>
<span data-ttu-id="103e6-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="103e6-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="103e6-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="103e6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="103e6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="103e6-128">CommonParameters</span></span>
<span data-ttu-id="103e6-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="103e6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="103e6-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="103e6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="103e6-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="103e6-131">INPUTS</span></span>

### <span data-ttu-id="103e6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="103e6-132">System.String</span></span>

## <span data-ttu-id="103e6-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="103e6-133">OUTPUTS</span></span>

### <span data-ttu-id="103e6-134">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="103e6-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="103e6-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="103e6-135">NOTES</span></span>

## <span data-ttu-id="103e6-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="103e6-136">RELATED LINKS</span></span>

[<span data-ttu-id="103e6-137">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="103e6-137">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)



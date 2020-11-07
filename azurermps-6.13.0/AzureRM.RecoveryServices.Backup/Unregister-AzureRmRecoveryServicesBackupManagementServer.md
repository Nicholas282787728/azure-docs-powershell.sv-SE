---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/unregister-azurermrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 4ef306b80aaf5fbb03b5ee4e98104829d8853ba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756137"
---
# <span data-ttu-id="d22c2-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="d22c2-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="d22c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d22c2-102">SYNOPSIS</span></span>
<span data-ttu-id="d22c2-103">Avregistrerar en SCDPM-Server eller reserv Server från valvet.</span><span class="sxs-lookup"><span data-stu-id="d22c2-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d22c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d22c2-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d22c2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d22c2-105">DESCRIPTION</span></span>
<span data-ttu-id="d22c2-106">Med cmdleten **Unregistered-AzureRmRecoveryServicesBackupManagementServer** avregistrerar du en System Center Data Protection Manager-Server (SCDPM) eller en Azure Backup-Server från valvet.</span><span class="sxs-lookup"><span data-stu-id="d22c2-106">The **Unregister-AzureRmRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="d22c2-107">Denna cmdlet tar bort referenser till de servrar som avregistrerats från valvet.</span><span class="sxs-lookup"><span data-stu-id="d22c2-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>
<span data-ttu-id="d22c2-108">Innan du kan avregistrera en behållare måste du ta bort alla skyddade data som är kopplade till den behållaren.</span><span class="sxs-lookup"><span data-stu-id="d22c2-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="d22c2-109">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d22c2-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d22c2-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d22c2-110">EXAMPLES</span></span>

### <span data-ttu-id="d22c2-111">Exempel 1: avregistrera en SCDPM-Server från valvet</span><span class="sxs-lookup"><span data-stu-id="d22c2-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```
PS C:\>$BMS = Get-AzureRmRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer $BMS
```

<span data-ttu-id="d22c2-112">Det första kommandot får säkerhets kopierings servern med namnet dpmserver01.contoso.com och lagrar den sedan i $BMS variabel.</span><span class="sxs-lookup"><span data-stu-id="d22c2-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>
<span data-ttu-id="d22c2-113">Det andra kommandot avregistrerar SCDPM-servern från valvet.</span><span class="sxs-lookup"><span data-stu-id="d22c2-113">The second command unregisters the SCDPM server from the vault.</span></span>

## <span data-ttu-id="d22c2-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d22c2-114">PARAMETERS</span></span>

### <span data-ttu-id="d22c2-115">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="d22c2-115">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="d22c2-116">Anger ett SCDPM-objekt som ska avregistreras.</span><span class="sxs-lookup"><span data-stu-id="d22c2-116">Specifies an SCDPM server object to unregister.</span></span>
<span data-ttu-id="d22c2-117">Använd Get-AzureRmRecoveryServicesBackupManagementServer cmdlet för att få ett **BackupManagementServer** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d22c2-117">To obtain an **BackupManagementServer** object, use the Get-AzureRmRecoveryServicesBackupManagementServer cmdlet.</span></span>

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

### <span data-ttu-id="d22c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d22c2-118">-DefaultProfile</span></span>
<span data-ttu-id="d22c2-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d22c2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d22c2-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d22c2-120">-PassThru</span></span>
<span data-ttu-id="d22c2-121">Returnera säkerhets kopierings hanterings servern som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d22c2-121">Return the Backup Management Server to be deleted.</span></span>

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

### <span data-ttu-id="d22c2-122">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d22c2-122">-VaultId</span></span>
<span data-ttu-id="d22c2-123">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="d22c2-123">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d22c2-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d22c2-124">-Confirm</span></span>
<span data-ttu-id="d22c2-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d22c2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d22c2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d22c2-126">-WhatIf</span></span>
<span data-ttu-id="d22c2-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d22c2-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d22c2-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d22c2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d22c2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d22c2-129">CommonParameters</span></span>
<span data-ttu-id="d22c2-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d22c2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d22c2-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d22c2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d22c2-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d22c2-132">INPUTS</span></span>

### <span data-ttu-id="d22c2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d22c2-133">System.String</span></span>
<span data-ttu-id="d22c2-134">Parametrar: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d22c2-134">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="d22c2-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d22c2-135">OUTPUTS</span></span>

### <span data-ttu-id="d22c2-136">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="d22c2-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="d22c2-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d22c2-137">NOTES</span></span>

## <span data-ttu-id="d22c2-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d22c2-138">RELATED LINKS</span></span>

[<span data-ttu-id="d22c2-139">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="d22c2-139">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)



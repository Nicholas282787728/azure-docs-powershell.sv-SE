---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 1b025825878e2bc97837237e194b0ec37eb298d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582271"
---
# <span data-ttu-id="3703d-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="3703d-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="3703d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3703d-102">SYNOPSIS</span></span>
<span data-ttu-id="3703d-103">Avregistrerar en SCDPM-Server eller reserv Server från valvet.</span><span class="sxs-lookup"><span data-stu-id="3703d-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3703d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3703d-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3703d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3703d-105">DESCRIPTION</span></span>
<span data-ttu-id="3703d-106">Med cmdleten **Unregistered-AzureRmRecoveryServicesBackupManagementServer** avregistrerar du en System Center Data Protection Manager-Server (SCDPM) eller en Azure Backup-Server från valvet.</span><span class="sxs-lookup"><span data-stu-id="3703d-106">The **Unregister-AzureRmRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="3703d-107">Denna cmdlet tar bort referenser till de servrar som avregistrerats från valvet.</span><span class="sxs-lookup"><span data-stu-id="3703d-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>

<span data-ttu-id="3703d-108">Innan du kan avregistrera en behållare måste du ta bort alla skyddade data som är kopplade till den behållaren.</span><span class="sxs-lookup"><span data-stu-id="3703d-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

<span data-ttu-id="3703d-109">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3703d-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="3703d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3703d-110">EXAMPLES</span></span>

### <span data-ttu-id="3703d-111">Exempel 1: avregistrera en SCDPM-Server från valvet</span><span class="sxs-lookup"><span data-stu-id="3703d-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```
PS C:\>$BMS = Get-AzureRmRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer $BMS
```

<span data-ttu-id="3703d-112">Det första kommandot får säkerhets kopierings servern med namnet dpmserver01.contoso.com och lagrar den sedan i $BMS variabel.</span><span class="sxs-lookup"><span data-stu-id="3703d-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>

<span data-ttu-id="3703d-113">Det andra kommandot avregistrerar SCDPM-servern från valvet.</span><span class="sxs-lookup"><span data-stu-id="3703d-113">The second command unregisters the SCDPM server from the vault.</span></span>

## <span data-ttu-id="3703d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3703d-114">PARAMETERS</span></span>

### <span data-ttu-id="3703d-115">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="3703d-115">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="3703d-116">Anger ett SCDPM-objekt som ska avregistreras.</span><span class="sxs-lookup"><span data-stu-id="3703d-116">Specifies an SCDPM server object to unregister.</span></span>
<span data-ttu-id="3703d-117">Använd Get-AzureRmRecoveryServicesBackupManagementServer cmdlet för att få ett **BackupManagementServer** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3703d-117">To obtain an **BackupManagementServer** object, use the Get-AzureRmRecoveryServicesBackupManagementServer cmdlet.</span></span>

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

### <span data-ttu-id="3703d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3703d-118">-DefaultProfile</span></span>
<span data-ttu-id="3703d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3703d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3703d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3703d-120">CommonParameters</span></span>
<span data-ttu-id="3703d-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3703d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3703d-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3703d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3703d-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3703d-123">INPUTS</span></span>

## <span data-ttu-id="3703d-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3703d-124">OUTPUTS</span></span>

## <span data-ttu-id="3703d-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3703d-125">NOTES</span></span>

## <span data-ttu-id="3703d-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3703d-126">RELATED LINKS</span></span>

[<span data-ttu-id="3703d-127">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="3703d-127">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)



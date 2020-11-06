---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: c3419f020aca0853d94d8848e944e39fc8ed05a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576822"
---
# <span data-ttu-id="00c1a-101">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="00c1a-101">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="00c1a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="00c1a-102">SYNOPSIS</span></span>
<span data-ttu-id="00c1a-103">Hämtar SCDPM och hanterings servrar för Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="00c1a-103">Gets SCDPM and Azure Backup management servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00c1a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="00c1a-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00c1a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="00c1a-105">DESCRIPTION</span></span>
<span data-ttu-id="00c1a-106">Cmdleten **Get-AzureRmRecoveryServicesBackupManagementServer** hämtar en lista över servrar för säkerhets kopierings hantering som är registrerade i ett valv.</span><span class="sxs-lookup"><span data-stu-id="00c1a-106">The **Get-AzureRmRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="00c1a-107">Det finns två typer av servrar för säkerhets kopiering: System Center Data Protection Manager (SCDPM) och Azure Backup Management Servers.</span><span class="sxs-lookup"><span data-stu-id="00c1a-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="00c1a-108">Servrar för säkerhets kopiering installeras separat för att hantera säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="00c1a-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="00c1a-109">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="00c1a-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="00c1a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="00c1a-110">EXAMPLES</span></span>

### <span data-ttu-id="00c1a-111">Exempel 1: Hämta alla servrar för säkerhets kopierings hantering</span><span class="sxs-lookup"><span data-stu-id="00c1a-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupManagementServer
```

<span data-ttu-id="00c1a-112">Det här kommandot får alla säkerhets kopierings servrar registrerade i valvet.</span><span class="sxs-lookup"><span data-stu-id="00c1a-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="00c1a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="00c1a-113">PARAMETERS</span></span>

### <span data-ttu-id="00c1a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00c1a-114">-DefaultProfile</span></span>
<span data-ttu-id="00c1a-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="00c1a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00c1a-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="00c1a-116">-Name</span></span>
<span data-ttu-id="00c1a-117">Anger namnet på den reserv Server för säkerhets kopiering som ska visas.</span><span class="sxs-lookup"><span data-stu-id="00c1a-117">Specifies the name of the Backup management server to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00c1a-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="00c1a-118">-VaultId</span></span>
<span data-ttu-id="00c1a-119">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="00c1a-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="00c1a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00c1a-120">CommonParameters</span></span>
<span data-ttu-id="00c1a-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00c1a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00c1a-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00c1a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00c1a-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="00c1a-123">INPUTS</span></span>

### <span data-ttu-id="00c1a-124">System. String</span><span class="sxs-lookup"><span data-stu-id="00c1a-124">System.String</span></span>
<span data-ttu-id="00c1a-125">Parametrar: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="00c1a-125">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="00c1a-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="00c1a-126">OUTPUTS</span></span>

### <span data-ttu-id="00c1a-127">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="00c1a-127">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="00c1a-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="00c1a-128">NOTES</span></span>

## <span data-ttu-id="00c1a-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="00c1a-129">RELATED LINKS</span></span>

[<span data-ttu-id="00c1a-130">Avregistrera-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="00c1a-130">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzureRmRecoveryServicesBackupManagementServer.md)



---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 0dac27b7e17a9336db198906cdfb60fb15738795
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574233"
---
# <span data-ttu-id="64b74-101">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="64b74-101">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="64b74-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="64b74-102">SYNOPSIS</span></span>
<span data-ttu-id="64b74-103">Hämtar SCDPM och hanterings servrar för Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="64b74-103">Gets SCDPM and Azure Backup management servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64b74-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="64b74-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupManagementServer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64b74-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="64b74-105">DESCRIPTION</span></span>
<span data-ttu-id="64b74-106">Cmdleten **Get-AzureRmRecoveryServicesBackupManagementServer** hämtar en lista över servrar för säkerhets kopierings hantering som är registrerade i ett valv.</span><span class="sxs-lookup"><span data-stu-id="64b74-106">The **Get-AzureRmRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>

<span data-ttu-id="64b74-107">Det finns två typer av servrar för säkerhets kopiering: System Center Data Protection Manager (SCDPM) och Azure Backup Management Servers.</span><span class="sxs-lookup"><span data-stu-id="64b74-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="64b74-108">Servrar för säkerhets kopiering installeras separat för att hantera säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="64b74-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>

<span data-ttu-id="64b74-109">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="64b74-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="64b74-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="64b74-110">EXAMPLES</span></span>

### <span data-ttu-id="64b74-111">Exempel 1: Hämta alla servrar för säkerhets kopierings hantering</span><span class="sxs-lookup"><span data-stu-id="64b74-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupManagementServer
```

<span data-ttu-id="64b74-112">Det här kommandot får alla säkerhets kopierings servrar registrerade i valvet.</span><span class="sxs-lookup"><span data-stu-id="64b74-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="64b74-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="64b74-113">PARAMETERS</span></span>

### <span data-ttu-id="64b74-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64b74-114">-DefaultProfile</span></span>
<span data-ttu-id="64b74-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="64b74-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b74-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="64b74-116">-Name</span></span>
<span data-ttu-id="64b74-117">Anger namnet på den reserv Server för säkerhets kopiering som ska visas.</span><span class="sxs-lookup"><span data-stu-id="64b74-117">Specifies the name of the Backup management server to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b74-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64b74-118">CommonParameters</span></span>
<span data-ttu-id="64b74-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64b74-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64b74-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64b74-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64b74-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="64b74-121">INPUTS</span></span>

### <span data-ttu-id="64b74-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="64b74-122">None</span></span>
<span data-ttu-id="64b74-123">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="64b74-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="64b74-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="64b74-124">OUTPUTS</span></span>

### <span data-ttu-id="64b74-125">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="64b74-125">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

### <span data-ttu-id="64b74-126">System. Collections. Generic. IList ' 1 [Microsoft. Azure. kommandon. RecoveryServices. backup. cmdletar. MODELES. BackupEngineBase]</span><span class="sxs-lookup"><span data-stu-id="64b74-126">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase]</span></span>

## <span data-ttu-id="64b74-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="64b74-127">NOTES</span></span>

## <span data-ttu-id="64b74-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="64b74-128">RELATED LINKS</span></span>

[<span data-ttu-id="64b74-129">Avregistrera-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="64b74-129">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzureRmRecoveryServicesBackupManagementServer.md)



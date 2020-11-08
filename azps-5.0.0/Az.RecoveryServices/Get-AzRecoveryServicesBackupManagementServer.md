---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 09d27926f489feea397c98a217840bb973e002ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263436"
---
# <span data-ttu-id="ec318-101">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="ec318-101">Get-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="ec318-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ec318-102">SYNOPSIS</span></span>
<span data-ttu-id="ec318-103">Hämtar SCDPM och hanterings servrar för Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="ec318-103">Gets SCDPM and Azure Backup management servers.</span></span>

## <span data-ttu-id="ec318-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ec318-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec318-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ec318-105">DESCRIPTION</span></span>
<span data-ttu-id="ec318-106">Cmdleten **Get-AzRecoveryServicesBackupManagementServer** hämtar en lista över servrar för säkerhets kopierings hantering som är registrerade i ett valv.</span><span class="sxs-lookup"><span data-stu-id="ec318-106">The **Get-AzRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="ec318-107">Det finns två typer av servrar för säkerhets kopiering: System Center Data Protection Manager (SCDPM) och Azure Backup Management Servers.</span><span class="sxs-lookup"><span data-stu-id="ec318-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="ec318-108">Servrar för säkerhets kopiering installeras separat för att hantera säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="ec318-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="ec318-109">Ställ in valv kontexten med hjälp av Set-AzRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ec318-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="ec318-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ec318-110">EXAMPLES</span></span>

### <span data-ttu-id="ec318-111">Exempel 1: Hämta alla servrar för säkerhets kopierings hantering</span><span class="sxs-lookup"><span data-stu-id="ec318-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

<span data-ttu-id="ec318-112">Det här kommandot får alla säkerhets kopierings servrar registrerade i valvet.</span><span class="sxs-lookup"><span data-stu-id="ec318-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="ec318-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ec318-113">PARAMETERS</span></span>

### <span data-ttu-id="ec318-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec318-114">-DefaultProfile</span></span>
<span data-ttu-id="ec318-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ec318-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec318-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="ec318-116">-Name</span></span>
<span data-ttu-id="ec318-117">Anger namnet på den reserv Server för säkerhets kopiering som ska visas.</span><span class="sxs-lookup"><span data-stu-id="ec318-117">Specifies the name of the Backup management server to get.</span></span>

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

### <span data-ttu-id="ec318-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ec318-118">-VaultId</span></span>
<span data-ttu-id="ec318-119">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="ec318-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ec318-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec318-120">CommonParameters</span></span>
<span data-ttu-id="ec318-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec318-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec318-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec318-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec318-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ec318-123">INPUTS</span></span>

### <span data-ttu-id="ec318-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ec318-124">System.String</span></span>

## <span data-ttu-id="ec318-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ec318-125">OUTPUTS</span></span>

### <span data-ttu-id="ec318-126">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="ec318-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="ec318-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ec318-127">NOTES</span></span>

## <span data-ttu-id="ec318-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ec318-128">RELATED LINKS</span></span>

[<span data-ttu-id="ec318-129">Avregistrera-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="ec318-129">Unregister-AzRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzRecoveryServicesBackupManagementServer.md)



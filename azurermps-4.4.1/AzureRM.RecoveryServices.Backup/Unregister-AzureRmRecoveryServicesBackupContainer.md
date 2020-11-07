---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: c5ab79ca42096ab93102be1288c772cab1ac01f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756892"
---
# <span data-ttu-id="1b2ae-101">Unregister-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="1b2ae-101">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="1b2ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b2ae-102">SYNOPSIS</span></span>
<span data-ttu-id="1b2ae-103">Avregistrerar en Windows-Server eller annan behållare från valvet.</span><span class="sxs-lookup"><span data-stu-id="1b2ae-103">Unregisters a Windows Server or other container from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b2ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b2ae-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b2ae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b2ae-105">DESCRIPTION</span></span>
<span data-ttu-id="1b2ae-106">Med cmdleten **Unregistered-AzureRmRecoveryServicesBackupContainer** avregistrerar du en Windows Server eller annan säkerhets kopierings behållare från valvet.</span><span class="sxs-lookup"><span data-stu-id="1b2ae-106">The **Unregister-AzureRmRecoveryServicesBackupContainer** cmdlet unregisters a Windows Server or other Backup container from the vault.</span></span>
<span data-ttu-id="1b2ae-107">Denna cmdlet tar bort referenser till en behållare från valvet.</span><span class="sxs-lookup"><span data-stu-id="1b2ae-107">This cmdlet removes references to a container from the vault.</span></span>
<span data-ttu-id="1b2ae-108">Innan du kan avregistrera en behållare måste du ta bort alla skyddade data som är kopplade till den behållaren.</span><span class="sxs-lookup"><span data-stu-id="1b2ae-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

<span data-ttu-id="1b2ae-109">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1b2ae-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="1b2ae-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b2ae-110">EXAMPLES</span></span>

### <span data-ttu-id="1b2ae-111">Exempel 1: avregistrera en Windows Server från valvet</span><span class="sxs-lookup"><span data-stu-id="1b2ae-111">Example 1: Unregister a Windows Server from the vault</span></span>
```
PS C:\>$Cont = Get-AzureRmRecoveryServicesContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupContainer -Container $Cont
```

<span data-ttu-id="1b2ae-112">Det första kommandot hämtar Windows-behållaren med namnet server01.contoso.com som är registrerad i valvet och lagrar det sedan i $Cont variabel.</span><span class="sxs-lookup"><span data-stu-id="1b2ae-112">The first command gets the Windows container named server01.contoso.com that is registered in the vault, and then stores it in the $Cont variable.</span></span>

<span data-ttu-id="1b2ae-113">Det andra kommandot avregistrerar den angivna Windows-servern från Azure Backup-valvet.</span><span class="sxs-lookup"><span data-stu-id="1b2ae-113">The second command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

## <span data-ttu-id="1b2ae-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b2ae-114">PARAMETERS</span></span>

### <span data-ttu-id="1b2ae-115">-Container</span><span class="sxs-lookup"><span data-stu-id="1b2ae-115">-Container</span></span>
<span data-ttu-id="1b2ae-116">Anger ett säkerhets kopierings objekt som ska avregistreras.</span><span class="sxs-lookup"><span data-stu-id="1b2ae-116">Specifies a Backup container object to unregister.</span></span>
<span data-ttu-id="1b2ae-117">För att hämta ett **BackupContainer** -objekt, Använd cmdleten Get-AzureRmRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="1b2ae-117">To obtain a **BackupContainer** object, use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b2ae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b2ae-118">-DefaultProfile</span></span>
<span data-ttu-id="1b2ae-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1b2ae-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b2ae-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b2ae-120">CommonParameters</span></span>
<span data-ttu-id="1b2ae-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b2ae-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b2ae-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b2ae-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b2ae-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b2ae-123">INPUTS</span></span>

## <span data-ttu-id="1b2ae-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b2ae-124">OUTPUTS</span></span>

## <span data-ttu-id="1b2ae-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b2ae-125">NOTES</span></span>

## <span data-ttu-id="1b2ae-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b2ae-126">RELATED LINKS</span></span>

[<span data-ttu-id="1b2ae-127">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="1b2ae-127">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)



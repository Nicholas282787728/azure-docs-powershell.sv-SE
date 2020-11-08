---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: efe463bab4195dfb09692f76d0e02e3aeaa59344
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088610"
---
# <span data-ttu-id="d0d4d-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="d0d4d-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="d0d4d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0d4d-102">SYNOPSIS</span></span>
<span data-ttu-id="d0d4d-103">Hämtar egenskaper för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="d0d4d-103">Gets Backup properties.</span></span>

## <span data-ttu-id="d0d4d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0d4d-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0d4d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0d4d-105">DESCRIPTION</span></span>
<span data-ttu-id="d0d4d-106">Cmdleten **Get-AzRecoveryServicesBackupProperty** hämtar säkerhets kopierings egenskaper för ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="d0d4d-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="d0d4d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0d4d-107">EXAMPLES</span></span>

### <span data-ttu-id="d0d4d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d0d4d-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="d0d4d-109">Skaffa säkerhets kopierings valv egenskapen för valvet.</span><span class="sxs-lookup"><span data-stu-id="d0d4d-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="d0d4d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0d4d-110">PARAMETERS</span></span>

### <span data-ttu-id="d0d4d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0d4d-111">-DefaultProfile</span></span>
<span data-ttu-id="d0d4d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d0d4d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0d4d-113">-Valv</span><span class="sxs-lookup"><span data-stu-id="d0d4d-113">-Vault</span></span>
<span data-ttu-id="d0d4d-114">Anger namnet på valvet.</span><span class="sxs-lookup"><span data-stu-id="d0d4d-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="d0d4d-115">Valvet måste vara ett **AzureRmRecoveryServicesVault** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d0d4d-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0d4d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0d4d-116">CommonParameters</span></span>
<span data-ttu-id="d0d4d-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0d4d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0d4d-118">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0d4d-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0d4d-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0d4d-119">INPUTS</span></span>

### <span data-ttu-id="d0d4d-120">Microsoft. Azure. commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="d0d4d-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="d0d4d-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0d4d-121">OUTPUTS</span></span>

### <span data-ttu-id="d0d4d-122">Microsoft. Azure. commands. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="d0d4d-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="d0d4d-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0d4d-123">NOTES</span></span>

## <span data-ttu-id="d0d4d-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0d4d-124">RELATED LINKS</span></span>

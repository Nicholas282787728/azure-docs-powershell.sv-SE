---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
ms.openlocfilehash: d900da862572c0e3a51f288a7e6bec948f7aeba4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576128"
---
# <span data-ttu-id="c4dea-101">Get-AzureRmRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="c4dea-101">Get-AzureRmRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="c4dea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4dea-102">SYNOPSIS</span></span>
<span data-ttu-id="c4dea-103">Hämtar egenskaper för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="c4dea-103">Gets Backup properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4dea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4dea-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4dea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4dea-105">DESCRIPTION</span></span>
<span data-ttu-id="c4dea-106">Cmdleten **Get-AzureRmRecoveryServicesBackupProperty** hämtar säkerhets kopierings egenskaper för ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="c4dea-106">The **Get-AzureRmRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="c4dea-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4dea-107">EXAMPLES</span></span>

### <span data-ttu-id="c4dea-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c4dea-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="c4dea-109">Skaffa säkerhets kopierings valv egenskapen för valvet.</span><span class="sxs-lookup"><span data-stu-id="c4dea-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="c4dea-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4dea-110">PARAMETERS</span></span>

### <span data-ttu-id="c4dea-111">-Valv</span><span class="sxs-lookup"><span data-stu-id="c4dea-111">-Vault</span></span>
<span data-ttu-id="c4dea-112">Anger namnet på valvet.</span><span class="sxs-lookup"><span data-stu-id="c4dea-112">Specifies the name of the vault.</span></span>
<span data-ttu-id="c4dea-113">Valvet måste vara ett **AzureRmRecoveryServicesVault** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c4dea-113">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4dea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4dea-114">-DefaultProfile</span></span>
<span data-ttu-id="c4dea-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c4dea-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4dea-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4dea-116">CommonParameters</span></span>
<span data-ttu-id="c4dea-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4dea-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4dea-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4dea-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4dea-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4dea-119">INPUTS</span></span>

### <span data-ttu-id="c4dea-120">Microsoft. Azure. commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="c4dea-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="c4dea-121">Parametrar: valv (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c4dea-121">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="c4dea-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4dea-122">OUTPUTS</span></span>

### <span data-ttu-id="c4dea-123">Microsoft. Azure. commands. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="c4dea-123">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="c4dea-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4dea-124">NOTES</span></span>

## <span data-ttu-id="c4dea-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4dea-125">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
ms.openlocfilehash: 3e93df0adfe1e1bc10d5ea74dd189bee60595824
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756872"
---
# <span data-ttu-id="d8cbc-101">Get-AzureRmRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="d8cbc-101">Get-AzureRmRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="d8cbc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8cbc-102">SYNOPSIS</span></span>
<span data-ttu-id="d8cbc-103">Hämtar egenskaper för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="d8cbc-103">Gets Backup properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8cbc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8cbc-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8cbc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8cbc-105">DESCRIPTION</span></span>
<span data-ttu-id="d8cbc-106">Cmdleten **Get-AzureRmRecoveryServicesBackupProperty** hämtar säkerhets kopierings egenskaper för ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="d8cbc-106">The **Get-AzureRmRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="d8cbc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8cbc-107">EXAMPLES</span></span>

## <span data-ttu-id="d8cbc-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8cbc-108">PARAMETERS</span></span>

### <span data-ttu-id="d8cbc-109">-Valv</span><span class="sxs-lookup"><span data-stu-id="d8cbc-109">-Vault</span></span>
<span data-ttu-id="d8cbc-110">Anger namnet på valvet.</span><span class="sxs-lookup"><span data-stu-id="d8cbc-110">Specifies the name of the vault.</span></span>
<span data-ttu-id="d8cbc-111">Valvet måste vara ett **AzureRmRecoveryServicesVault** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d8cbc-111">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="d8cbc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8cbc-112">-DefaultProfile</span></span>
<span data-ttu-id="d8cbc-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d8cbc-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8cbc-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8cbc-114">CommonParameters</span></span>
<span data-ttu-id="d8cbc-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8cbc-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8cbc-116">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8cbc-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8cbc-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8cbc-117">INPUTS</span></span>

### <span data-ttu-id="d8cbc-118">Microsoft. Azure. commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="d8cbc-118">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="d8cbc-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8cbc-119">OUTPUTS</span></span>

### <span data-ttu-id="d8cbc-120">Microsoft. Azure. commands. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="d8cbc-120">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="d8cbc-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8cbc-121">NOTES</span></span>

## <span data-ttu-id="d8cbc-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8cbc-122">RELATED LINKS</span></span>


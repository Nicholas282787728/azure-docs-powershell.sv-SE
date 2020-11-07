---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/set-azurermrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
ms.openlocfilehash: 9329f35377731eeb3e59e01a673129b5505abf49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756474"
---
# <span data-ttu-id="f9070-101">Set-AzureRmRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="f9070-101">Set-AzureRmRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="f9070-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f9070-102">SYNOPSIS</span></span>
<span data-ttu-id="f9070-103">Anger valv kontext.</span><span class="sxs-lookup"><span data-stu-id="f9070-103">Sets vault context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9070-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f9070-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9070-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f9070-105">DESCRIPTION</span></span>
<span data-ttu-id="f9070-106">Cmdleten **set-AzureRmRecoveryServicesVaultContext** anger valv kontexten för Azure Site Recovery-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="f9070-106">The **Set-AzureRmRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="f9070-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f9070-107">EXAMPLES</span></span>

### <span data-ttu-id="f9070-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f9070-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="f9070-109">Anger valv kontext.</span><span class="sxs-lookup"><span data-stu-id="f9070-109">Sets vault context.</span></span>

## <span data-ttu-id="f9070-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f9070-110">PARAMETERS</span></span>

### <span data-ttu-id="f9070-111">-Valv</span><span class="sxs-lookup"><span data-stu-id="f9070-111">-Vault</span></span>
<span data-ttu-id="f9070-112">Anger namnet på valvet.</span><span class="sxs-lookup"><span data-stu-id="f9070-112">Specifies the name of the vault.</span></span>
<span data-ttu-id="f9070-113">Valvet måste vara ett **AzureRmRecoveryServicesVault** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f9070-113">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="f9070-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9070-114">-DefaultProfile</span></span>
<span data-ttu-id="f9070-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f9070-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9070-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9070-116">CommonParameters</span></span>
<span data-ttu-id="f9070-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9070-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9070-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9070-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9070-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f9070-119">INPUTS</span></span>

### <span data-ttu-id="f9070-120">ARSVault</span><span class="sxs-lookup"><span data-stu-id="f9070-120">ARSVault</span></span>
<span data-ttu-id="f9070-121">Parametern ' valv ' godkänner värdet av typen ' ARSVault ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f9070-121">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="f9070-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f9070-122">OUTPUTS</span></span>

## <span data-ttu-id="f9070-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f9070-123">NOTES</span></span>

## <span data-ttu-id="f9070-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f9070-124">RELATED LINKS</span></span>


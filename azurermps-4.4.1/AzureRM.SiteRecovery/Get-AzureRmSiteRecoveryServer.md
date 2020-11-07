---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: CFB7CF64-1415-44B3-932B-2A5613666D3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: aacb061772ed1b1202528ebc7b7bc95d725bb9f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757450"
---
# <span data-ttu-id="80656-101">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="80656-101">Get-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="80656-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="80656-102">SYNOPSIS</span></span>
<span data-ttu-id="80656-103">Hämtar information om återställnings servrar registrerade för det aktuella valvet.</span><span class="sxs-lookup"><span data-stu-id="80656-103">Gets information about Site Recovery servers registered to the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80656-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="80656-104">SYNTAX</span></span>

### <span data-ttu-id="80656-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="80656-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80656-106">ByName</span><span class="sxs-lookup"><span data-stu-id="80656-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServer -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80656-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="80656-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="80656-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="80656-108">DESCRIPTION</span></span>
<span data-ttu-id="80656-109">Cmdleten **Get-AzureRmSiteRecoveryServer** hämtar information om Azure Site Recovery-servrar registrerade till det aktuella Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="80656-109">The **Get-AzureRmSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="80656-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="80656-110">EXAMPLES</span></span>

## <span data-ttu-id="80656-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="80656-111">PARAMETERS</span></span>

### <span data-ttu-id="80656-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="80656-112">-FriendlyName</span></span>
<span data-ttu-id="80656-113">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="80656-113">Specifies the friendly name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80656-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="80656-114">-Name</span></span>
<span data-ttu-id="80656-115">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="80656-115">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80656-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80656-116">-DefaultProfile</span></span>
<span data-ttu-id="80656-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="80656-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80656-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80656-118">CommonParameters</span></span>
<span data-ttu-id="80656-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80656-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80656-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80656-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80656-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="80656-121">INPUTS</span></span>

## <span data-ttu-id="80656-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="80656-122">OUTPUTS</span></span>

### <span data-ttu-id="80656-123">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="80656-123">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="80656-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="80656-124">NOTES</span></span>

## <span data-ttu-id="80656-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="80656-125">RELATED LINKS</span></span>

[<span data-ttu-id="80656-126">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="80656-126">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)

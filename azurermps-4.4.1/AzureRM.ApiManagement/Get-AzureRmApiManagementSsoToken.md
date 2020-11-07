---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
ms.openlocfilehash: 7ca683fc8b4c84a31a651982e5b605d3c29123a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755308"
---
# <span data-ttu-id="db876-101">Get-AzureRmApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="db876-101">Get-AzureRmApiManagementSsoToken</span></span>

## <span data-ttu-id="db876-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db876-102">SYNOPSIS</span></span>
<span data-ttu-id="db876-103">Hämtar en länk med SSO-token till en distribuerad hanterings Portal för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="db876-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db876-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db876-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db876-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db876-105">DESCRIPTION</span></span>
<span data-ttu-id="db876-106">Cmdleten **Get-AzureRmApiManagementSsoToken** returnerar en länk (URL) som innehåller en token för enkel inloggning (SSO) till en distribuerad hanterings Portal för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="db876-106">The **Get-AzureRmApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="db876-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db876-107">EXAMPLES</span></span>

### <span data-ttu-id="db876-108">Exempel 1: Hämta SSO-token för en API-hanterings tjänst</span><span class="sxs-lookup"><span data-stu-id="db876-108">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzureRmApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="db876-109">Det här kommandot får SSO-token för en API-hanterings tjänst.</span><span class="sxs-lookup"><span data-stu-id="db876-109">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="db876-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db876-110">PARAMETERS</span></span>

### <span data-ttu-id="db876-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="db876-111">-Name</span></span>
<span data-ttu-id="db876-112">Anger namnet på API-hanterings instansen.</span><span class="sxs-lookup"><span data-stu-id="db876-112">Specifies the name of the API Management instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db876-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db876-113">-ResourceGroupName</span></span>
<span data-ttu-id="db876-114">Anger namnet på den resurs grupp som API-hantering finns under.</span><span class="sxs-lookup"><span data-stu-id="db876-114">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db876-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db876-115">-DefaultProfile</span></span>
<span data-ttu-id="db876-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="db876-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db876-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db876-117">CommonParameters</span></span>
<span data-ttu-id="db876-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db876-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db876-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db876-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db876-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db876-120">INPUTS</span></span>

## <span data-ttu-id="db876-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db876-121">OUTPUTS</span></span>

### <span data-ttu-id="db876-122">System. String</span><span class="sxs-lookup"><span data-stu-id="db876-122">System.String</span></span>

## <span data-ttu-id="db876-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db876-123">NOTES</span></span>

## <span data-ttu-id="db876-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db876-124">RELATED LINKS</span></span>

[<span data-ttu-id="db876-125">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="db876-125">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


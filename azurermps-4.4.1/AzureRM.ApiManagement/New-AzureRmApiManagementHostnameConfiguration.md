---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D4C465CE-1B8A-4CFC-BAA8-21CC66B7D6D6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
ms.openlocfilehash: 1b34903f402f7e8d432d16087f1e32fc7b7da3e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578631"
---
# <span data-ttu-id="873a0-101">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="873a0-101">New-AzureRmApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="873a0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="873a0-102">SYNOPSIS</span></span>
<span data-ttu-id="873a0-103">Skapar en instans av PsApiManagementHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="873a0-103">Creates an instance of PsApiManagementHostnameConfiguration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="873a0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="873a0-104">SYNTAX</span></span>

```
New-AzureRmApiManagementHostnameConfiguration -CertificateThumbprint <String> -Hostname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="873a0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="873a0-105">DESCRIPTION</span></span>
<span data-ttu-id="873a0-106">**New-AzureRmApiManagementHostnameConfiguration** cmdlet är ett hjälp kommando som skapar en instans av **PsApiManagementHostnameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="873a0-106">The **New-AzureRmApiManagementHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementHostnameConfiguration**.</span></span>
<span data-ttu-id="873a0-107">Det här kommandot används med Set-AzureRmApiManagementHostnames cmdlet.</span><span class="sxs-lookup"><span data-stu-id="873a0-107">This command is used with the Set-AzureRmApiManagementHostnames cmdlet.</span></span>

## <span data-ttu-id="873a0-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="873a0-108">EXAMPLES</span></span>

### <span data-ttu-id="873a0-109">Exempel 1: skapa och initiera en instans av PsApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="873a0-109">Example 1: Create and initialize an instance of PsApiManagementHostnameConfiguration</span></span>
```
PS C:\>New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
```

<span data-ttu-id="873a0-110">Det här kommandot skapar och initierar en instans av **PsApiManagementHostnameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="873a0-110">This command creates and initializes an instance of **PsApiManagementHostnameConfiguration**.</span></span>

## <span data-ttu-id="873a0-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="873a0-111">PARAMETERS</span></span>

### <span data-ttu-id="873a0-112">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="873a0-112">-CertificateThumbprint</span></span>
<span data-ttu-id="873a0-113">Anger tumavtryck för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="873a0-113">Specifies the certificate thumbprint.</span></span>
<span data-ttu-id="873a0-114">Certifikatet måste först importeras med Import-AzureRmApiManagementHostnameCertificate cmdlet.</span><span class="sxs-lookup"><span data-stu-id="873a0-114">The certificate must be first imported with the Import-AzureRmApiManagementHostnameCertificate cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="873a0-115">-Hostname</span><span class="sxs-lookup"><span data-stu-id="873a0-115">-Hostname</span></span>
<span data-ttu-id="873a0-116">Anger det anpassade värd namnet som denna cmdlet skapar **PsApiManagementHostnameConfiguration** -instansen för.</span><span class="sxs-lookup"><span data-stu-id="873a0-116">Specifies the custom host name for which this cmdlet creates the **PsApiManagementHostnameConfiguration** instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="873a0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="873a0-117">-DefaultProfile</span></span>
<span data-ttu-id="873a0-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="873a0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="873a0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="873a0-119">CommonParameters</span></span>
<span data-ttu-id="873a0-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="873a0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="873a0-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="873a0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="873a0-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="873a0-122">INPUTS</span></span>

## <span data-ttu-id="873a0-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="873a0-123">OUTPUTS</span></span>

### <span data-ttu-id="873a0-124">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="873a0-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="873a0-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="873a0-125">NOTES</span></span>

## <span data-ttu-id="873a0-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="873a0-126">RELATED LINKS</span></span>

[<span data-ttu-id="873a0-127">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="873a0-127">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="873a0-128">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="873a0-128">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)



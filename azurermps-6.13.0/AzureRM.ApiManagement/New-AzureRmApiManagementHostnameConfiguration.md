---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D4C465CE-1B8A-4CFC-BAA8-21CC66B7D6D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
ms.openlocfilehash: defd5c046427115e44783d6b34ea7b034edc8317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574080"
---
# <span data-ttu-id="da442-101">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="da442-101">New-AzureRmApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="da442-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da442-102">SYNOPSIS</span></span>
<span data-ttu-id="da442-103">Skapar en instans av PsApiManagementHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="da442-103">Creates an instance of PsApiManagementHostnameConfiguration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da442-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da442-104">SYNTAX</span></span>

```
New-AzureRmApiManagementHostnameConfiguration -CertificateThumbprint <String> -Hostname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da442-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da442-105">DESCRIPTION</span></span>
<span data-ttu-id="da442-106">**New-AzureRmApiManagementHostnameConfiguration** cmdlet är ett hjälp kommando som skapar en instans av **PsApiManagementHostnameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="da442-106">The **New-AzureRmApiManagementHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementHostnameConfiguration**.</span></span>
<span data-ttu-id="da442-107">Det här kommandot används med Set-AzureRmApiManagementHostnames cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da442-107">This command is used with the Set-AzureRmApiManagementHostnames cmdlet.</span></span>

## <span data-ttu-id="da442-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da442-108">EXAMPLES</span></span>

### <span data-ttu-id="da442-109">Exempel 1: skapa och initiera en instans av PsApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="da442-109">Example 1: Create and initialize an instance of PsApiManagementHostnameConfiguration</span></span>
```
PS C:\>New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
```

<span data-ttu-id="da442-110">Det här kommandot skapar och initierar en instans av **PsApiManagementHostnameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="da442-110">This command creates and initializes an instance of **PsApiManagementHostnameConfiguration**.</span></span>

## <span data-ttu-id="da442-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da442-111">PARAMETERS</span></span>

### <span data-ttu-id="da442-112">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="da442-112">-CertificateThumbprint</span></span>
<span data-ttu-id="da442-113">Anger tumavtryck för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="da442-113">Specifies the certificate thumbprint.</span></span>
<span data-ttu-id="da442-114">Certifikatet måste först importeras med Import-AzureRmApiManagementHostnameCertificate cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da442-114">The certificate must be first imported with the Import-AzureRmApiManagementHostnameCertificate cmdlet.</span></span>

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

### <span data-ttu-id="da442-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da442-115">-DefaultProfile</span></span>
<span data-ttu-id="da442-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="da442-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da442-117">-Hostname</span><span class="sxs-lookup"><span data-stu-id="da442-117">-Hostname</span></span>
<span data-ttu-id="da442-118">Anger det anpassade värd namnet som denna cmdlet skapar **PsApiManagementHostnameConfiguration** -instansen för.</span><span class="sxs-lookup"><span data-stu-id="da442-118">Specifies the custom host name for which this cmdlet creates the **PsApiManagementHostnameConfiguration** instance.</span></span>

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

### <span data-ttu-id="da442-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da442-119">CommonParameters</span></span>
<span data-ttu-id="da442-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da442-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da442-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da442-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da442-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da442-122">INPUTS</span></span>

### <span data-ttu-id="da442-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="da442-123">None</span></span>

## <span data-ttu-id="da442-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da442-124">OUTPUTS</span></span>

### <span data-ttu-id="da442-125">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="da442-125">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="da442-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da442-126">NOTES</span></span>

## <span data-ttu-id="da442-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da442-127">RELATED LINKS</span></span>

[<span data-ttu-id="da442-128">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="da442-128">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="da442-129">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="da442-129">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)



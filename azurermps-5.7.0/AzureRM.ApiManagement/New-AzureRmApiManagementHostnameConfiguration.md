---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: D4C465CE-1B8A-4CFC-BAA8-21CC66B7D6D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
ms.openlocfilehash: 066538db3a763c5a3c6d9de9f621ca2b81552983
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573583"
---
# <span data-ttu-id="522f8-101">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="522f8-101">New-AzureRmApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="522f8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="522f8-102">SYNOPSIS</span></span>
<span data-ttu-id="522f8-103">Skapar en instans av PsApiManagementHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="522f8-103">Creates an instance of PsApiManagementHostnameConfiguration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="522f8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="522f8-104">SYNTAX</span></span>

```
New-AzureRmApiManagementHostnameConfiguration -CertificateThumbprint <String> -Hostname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="522f8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="522f8-105">DESCRIPTION</span></span>
<span data-ttu-id="522f8-106">**New-AzureRmApiManagementHostnameConfiguration** cmdlet är ett hjälp kommando som skapar en instans av **PsApiManagementHostnameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="522f8-106">The **New-AzureRmApiManagementHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementHostnameConfiguration**.</span></span>
<span data-ttu-id="522f8-107">Det här kommandot används med Set-AzureRmApiManagementHostnames cmdlet.</span><span class="sxs-lookup"><span data-stu-id="522f8-107">This command is used with the Set-AzureRmApiManagementHostnames cmdlet.</span></span>

## <span data-ttu-id="522f8-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="522f8-108">EXAMPLES</span></span>

### <span data-ttu-id="522f8-109">Exempel 1: skapa och initiera en instans av PsApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="522f8-109">Example 1: Create and initialize an instance of PsApiManagementHostnameConfiguration</span></span>
```
PS C:\>New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
```

<span data-ttu-id="522f8-110">Det här kommandot skapar och initierar en instans av **PsApiManagementHostnameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="522f8-110">This command creates and initializes an instance of **PsApiManagementHostnameConfiguration**.</span></span>

## <span data-ttu-id="522f8-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="522f8-111">PARAMETERS</span></span>

### <span data-ttu-id="522f8-112">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="522f8-112">-CertificateThumbprint</span></span>
<span data-ttu-id="522f8-113">Anger tumavtryck för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="522f8-113">Specifies the certificate thumbprint.</span></span>
<span data-ttu-id="522f8-114">Certifikatet måste först importeras med Import-AzureRmApiManagementHostnameCertificate cmdlet.</span><span class="sxs-lookup"><span data-stu-id="522f8-114">The certificate must be first imported with the Import-AzureRmApiManagementHostnameCertificate cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="522f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="522f8-115">-DefaultProfile</span></span>
<span data-ttu-id="522f8-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="522f8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="522f8-117">-Hostname</span><span class="sxs-lookup"><span data-stu-id="522f8-117">-Hostname</span></span>
<span data-ttu-id="522f8-118">Anger det anpassade värd namnet som denna cmdlet skapar **PsApiManagementHostnameConfiguration** -instansen för.</span><span class="sxs-lookup"><span data-stu-id="522f8-118">Specifies the custom host name for which this cmdlet creates the **PsApiManagementHostnameConfiguration** instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="522f8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="522f8-119">CommonParameters</span></span>
<span data-ttu-id="522f8-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="522f8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="522f8-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="522f8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="522f8-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="522f8-122">INPUTS</span></span>

### <span data-ttu-id="522f8-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="522f8-123">None</span></span>
<span data-ttu-id="522f8-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="522f8-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="522f8-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="522f8-125">OUTPUTS</span></span>

### <span data-ttu-id="522f8-126">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="522f8-126">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="522f8-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="522f8-127">NOTES</span></span>

## <span data-ttu-id="522f8-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="522f8-128">RELATED LINKS</span></span>

[<span data-ttu-id="522f8-129">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="522f8-129">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="522f8-130">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="522f8-130">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)



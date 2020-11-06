---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSystemCertificate.md
ms.openlocfilehash: fa64e9bade3a6cd8ec4edc8e04956c97306328ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573079"
---
# <span data-ttu-id="94941-101">New-AzureRmApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="94941-101">New-AzureRmApiManagementSystemCertificate</span></span>

## <span data-ttu-id="94941-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="94941-102">SYNOPSIS</span></span>
<span data-ttu-id="94941-103">Skapar en instans av `PsApiManagementSystemCertificate` .</span><span class="sxs-lookup"><span data-stu-id="94941-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="94941-104">Certifikatet kan utfärdas av en privat certifikat utfärdare och installeras i API-hanteringskonsolen i `CertificateAuthority` eller `Root` lagras.</span><span class="sxs-lookup"><span data-stu-id="94941-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94941-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="94941-105">SYNTAX</span></span>

```
New-AzureRmApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94941-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="94941-106">DESCRIPTION</span></span>
<span data-ttu-id="94941-107">**New-AzureRmApiManagementSystemCertificate** cmdlet är ett hjälp kommando som skapar en instans av **PsApiManagementSystemCertificate**.</span><span class="sxs-lookup"><span data-stu-id="94941-107">The **New-AzureRmApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="94941-108">Kommandot används med cmdleten New-AzureRmApiManagement och Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="94941-108">This command is used with the New-AzureRmApiManagement and Set-AzureRmApiManagement cmdlet.</span></span>

## <span data-ttu-id="94941-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="94941-109">EXAMPLES</span></span>

### <span data-ttu-id="94941-110">Exempel 1: skapa och initiera en instans av PsApiManagementSystemCertificate med ett SSL-certifikat från en fil</span><span class="sxs-lookup"><span data-stu-id="94941-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzureRmApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="94941-111">Det här kommandot skapar och initierar en instans av **PsApiManagementSystemCertificate** med ett rot certifikat.</span><span class="sxs-lookup"><span data-stu-id="94941-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="94941-112">Därefter skapas och API-hanterings tjänsten som installerar CERTIFIKATUTFÄRDARCERTIFIKATET till rot arkivet.</span><span class="sxs-lookup"><span data-stu-id="94941-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="94941-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="94941-113">PARAMETERS</span></span>

### <span data-ttu-id="94941-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94941-114">-DefaultProfile</span></span>
<span data-ttu-id="94941-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="94941-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94941-116">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="94941-116">-PfxPassword</span></span>
<span data-ttu-id="94941-117">Lösen ord för. pfx-filen.</span><span class="sxs-lookup"><span data-stu-id="94941-117">Password for the .pfx certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94941-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="94941-118">-PfxPath</span></span>
<span data-ttu-id="94941-119">Sökväg till en. pfx-fil.</span><span class="sxs-lookup"><span data-stu-id="94941-119">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="94941-120">-Butiks namn</span><span class="sxs-lookup"><span data-stu-id="94941-120">-StoreName</span></span>
<span data-ttu-id="94941-121">Butiks namn certifikat</span><span class="sxs-lookup"><span data-stu-id="94941-121">Certificate StoreName</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: CertificateAuthority, Root

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94941-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94941-122">CommonParameters</span></span>
<span data-ttu-id="94941-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94941-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94941-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94941-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94941-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="94941-125">INPUTS</span></span>

### <span data-ttu-id="94941-126">System. String</span><span class="sxs-lookup"><span data-stu-id="94941-126">System.String</span></span>

### <span data-ttu-id="94941-127">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="94941-127">System.Security.SecureString</span></span>

## <span data-ttu-id="94941-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="94941-128">OUTPUTS</span></span>

### <span data-ttu-id="94941-129">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="94941-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="94941-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="94941-130">NOTES</span></span>

## <span data-ttu-id="94941-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="94941-131">RELATED LINKS</span></span>

[<span data-ttu-id="94941-132">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="94941-132">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="94941-133">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="94941-133">Set-AzureRmApiManagement</span></span>](./Set-AzureRmApiManagement.md)

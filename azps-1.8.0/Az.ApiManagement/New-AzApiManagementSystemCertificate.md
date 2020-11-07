---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
ms.openlocfilehash: 54d2dba9c8db271fd495164049f2990a96a4b505
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917830"
---
# <span data-ttu-id="14603-101">New-AzApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="14603-101">New-AzApiManagementSystemCertificate</span></span>

## <span data-ttu-id="14603-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14603-102">SYNOPSIS</span></span>
<span data-ttu-id="14603-103">Skapar en instans av `PsApiManagementSystemCertificate` .</span><span class="sxs-lookup"><span data-stu-id="14603-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="14603-104">Certifikatet kan utfärdas av en privat certifikat utfärdare och installeras i API-hanteringskonsolen i `CertificateAuthority` eller `Root` lagras.</span><span class="sxs-lookup"><span data-stu-id="14603-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

## <span data-ttu-id="14603-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14603-105">SYNTAX</span></span>

```
New-AzApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14603-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14603-106">DESCRIPTION</span></span>
<span data-ttu-id="14603-107">**New-AzApiManagementSystemCertificate** cmdlet är ett hjälp kommando som skapar en instans av **PsApiManagementSystemCertificate**.</span><span class="sxs-lookup"><span data-stu-id="14603-107">The **New-AzApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="14603-108">Kommandot används med cmdleten New-AzApiManagement och Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="14603-108">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="14603-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14603-109">EXAMPLES</span></span>

### <span data-ttu-id="14603-110">Exempel 1: skapa och initiera en instans av PsApiManagementSystemCertificate med ett SSL-certifikat från en fil</span><span class="sxs-lookup"><span data-stu-id="14603-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="14603-111">Det här kommandot skapar och initierar en instans av **PsApiManagementSystemCertificate** med ett rot certifikat.</span><span class="sxs-lookup"><span data-stu-id="14603-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="14603-112">Därefter skapas och API-hanterings tjänsten som installerar CERTIFIKATUTFÄRDARCERTIFIKATET till rot arkivet.</span><span class="sxs-lookup"><span data-stu-id="14603-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="14603-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14603-113">PARAMETERS</span></span>

### <span data-ttu-id="14603-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14603-114">-DefaultProfile</span></span>
<span data-ttu-id="14603-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="14603-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14603-116">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="14603-116">-PfxPassword</span></span>
<span data-ttu-id="14603-117">Lösen ord för. pfx-filen.</span><span class="sxs-lookup"><span data-stu-id="14603-117">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="14603-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="14603-118">-PfxPath</span></span>
<span data-ttu-id="14603-119">Sökväg till en. pfx-fil.</span><span class="sxs-lookup"><span data-stu-id="14603-119">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="14603-120">-Butiks namn</span><span class="sxs-lookup"><span data-stu-id="14603-120">-StoreName</span></span>
<span data-ttu-id="14603-121">Butiks namn certifikat</span><span class="sxs-lookup"><span data-stu-id="14603-121">Certificate StoreName</span></span>

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

### <span data-ttu-id="14603-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14603-122">CommonParameters</span></span>
<span data-ttu-id="14603-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14603-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14603-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14603-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14603-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14603-125">INPUTS</span></span>

### <span data-ttu-id="14603-126">System. String</span><span class="sxs-lookup"><span data-stu-id="14603-126">System.String</span></span>

### <span data-ttu-id="14603-127">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="14603-127">System.Security.SecureString</span></span>

## <span data-ttu-id="14603-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14603-128">OUTPUTS</span></span>

### <span data-ttu-id="14603-129">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="14603-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="14603-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14603-130">NOTES</span></span>

## <span data-ttu-id="14603-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14603-131">RELATED LINKS</span></span>

[<span data-ttu-id="14603-132">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="14603-132">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="14603-133">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="14603-133">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)
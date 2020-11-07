---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: e22760c2838cf0b4fb0597dbd45532374b604b79
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929014"
---
# <span data-ttu-id="f3b42-101">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f3b42-101">New-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="f3b42-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3b42-102">SYNOPSIS</span></span>
<span data-ttu-id="f3b42-103">Skapar ett SSL-certifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f3b42-103">Creates an SSL certificate for an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3b42-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3b42-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3b42-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3b42-105">DESCRIPTION</span></span>
<span data-ttu-id="f3b42-106">Cmdleten **New-AzureRmApplicationGatewaySslCertificate** skapar ett SSL-certifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f3b42-106">The **New-AzureRmApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="f3b42-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3b42-107">EXAMPLES</span></span>

### <span data-ttu-id="f3b42-108">Exempel 1: skapa ett SSL-certifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f3b42-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="f3b42-109">Det här kommandot skapar ett SSL-certifikat med namnet Cert01 för standard program-gateway och lagrar resultatet i variabeln som heter $Cert.</span><span class="sxs-lookup"><span data-stu-id="f3b42-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="f3b42-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3b42-110">PARAMETERS</span></span>

### <span data-ttu-id="f3b42-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f3b42-111">-CertificateFile</span></span>
<span data-ttu-id="f3b42-112">Anger sökvägen till. pfx-filen för SSL-certifikatet som den här cmdleten skapar.</span><span class="sxs-lookup"><span data-stu-id="f3b42-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f3b42-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3b42-113">-DefaultProfile</span></span>
<span data-ttu-id="f3b42-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f3b42-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3b42-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="f3b42-115">-Name</span></span>
<span data-ttu-id="f3b42-116">Anger namnet på det SSL-certifikat som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="f3b42-116">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f3b42-117">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="f3b42-117">-Password</span></span>
<span data-ttu-id="f3b42-118">Anger lösen ordet för SSL som skapas av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3b42-118">Specifies the password of the SSL that this cmdlet creates.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3b42-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3b42-119">CommonParameters</span></span>
<span data-ttu-id="f3b42-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3b42-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3b42-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3b42-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3b42-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3b42-122">INPUTS</span></span>

### <span data-ttu-id="f3b42-123">System. String</span><span class="sxs-lookup"><span data-stu-id="f3b42-123">System.String</span></span>

## <span data-ttu-id="f3b42-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3b42-124">OUTPUTS</span></span>

### <span data-ttu-id="f3b42-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f3b42-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="f3b42-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3b42-126">NOTES</span></span>

## <span data-ttu-id="f3b42-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3b42-127">RELATED LINKS</span></span>

[<span data-ttu-id="f3b42-128">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f3b42-128">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="f3b42-129">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f3b42-129">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="f3b42-130">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f3b42-130">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="f3b42-131">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f3b42-131">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)



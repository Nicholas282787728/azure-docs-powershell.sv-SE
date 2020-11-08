---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
ms.openlocfilehash: e348d29a805de900aa3144832084e657cf85077c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092179"
---
# <span data-ttu-id="f6c86-101">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="f6c86-101">Get-AzWebAppCertificate</span></span>

## <span data-ttu-id="f6c86-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6c86-102">SYNOPSIS</span></span>
<span data-ttu-id="f6c86-103">Hämtar ett Azure Web App-certifikat.</span><span class="sxs-lookup"><span data-stu-id="f6c86-103">Gets an Azure Web App certificate.</span></span>

## <span data-ttu-id="f6c86-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6c86-104">SYNTAX</span></span>

```
Get-AzWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6c86-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6c86-105">DESCRIPTION</span></span>
<span data-ttu-id="f6c86-106">Cmdleten **Get-AzWebAppCertificate** hämtar information om Azure Web App-certifikat som är associerade med en viss resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f6c86-106">The **Get-AzWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="f6c86-107">Om du känner till tumavtryck för certifikatet kan du även använda denna cmdlet för att få information om ett visst certifikat.</span><span class="sxs-lookup"><span data-stu-id="f6c86-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="f6c86-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6c86-108">EXAMPLES</span></span>

### <span data-ttu-id="f6c86-109">Exempel 1: Hämta webb program certifikat i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="f6c86-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="f6c86-110">Det här kommandot returnerar information om de laddade webb program certifikat som är kopplade till resurs gruppen ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f6c86-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="f6c86-111">Exempel 2: Hämta ett angivet webb program certifikat</span><span class="sxs-lookup"><span data-stu-id="f6c86-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="f6c86-112">Det här kommandot får ContosoResourceGroup-certifikatet med tumavtrycket E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span><span class="sxs-lookup"><span data-stu-id="f6c86-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="f6c86-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6c86-113">PARAMETERS</span></span>

### <span data-ttu-id="f6c86-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6c86-114">-DefaultProfile</span></span>
<span data-ttu-id="f6c86-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f6c86-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6c86-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6c86-116">-ResourceGroupName</span></span>
<span data-ttu-id="f6c86-117">Anger namnet på resurs gruppen som certifikatet har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="f6c86-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6c86-118">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="f6c86-118">-Thumbprint</span></span>
<span data-ttu-id="f6c86-119">Anger det unika ID: t för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="f6c86-119">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6c86-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6c86-120">CommonParameters</span></span>
<span data-ttu-id="f6c86-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6c86-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6c86-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6c86-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6c86-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6c86-123">INPUTS</span></span>

### <span data-ttu-id="f6c86-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="f6c86-124">None</span></span>

## <span data-ttu-id="f6c86-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6c86-125">OUTPUTS</span></span>

### <span data-ttu-id="f6c86-126">Microsoft. Azure. commands. webapps. Models. WebApp. PSCertificate</span><span class="sxs-lookup"><span data-stu-id="f6c86-126">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="f6c86-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6c86-127">NOTES</span></span>

## <span data-ttu-id="f6c86-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6c86-128">RELATED LINKS</span></span>

[<span data-ttu-id="f6c86-129">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="f6c86-129">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)



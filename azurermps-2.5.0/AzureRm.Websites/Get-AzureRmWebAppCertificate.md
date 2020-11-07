---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappcertificate
schema: 2.0.0
ms.openlocfilehash: dcdba23de872ed0f1518188387c6f7e2d357c909
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929193"
---
# <span data-ttu-id="f61e2-101">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="f61e2-101">Get-AzureRmWebAppCertificate</span></span>

## <span data-ttu-id="f61e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f61e2-102">SYNOPSIS</span></span>
<span data-ttu-id="f61e2-103">Hämtar ett Azure Web App-certifikat.</span><span class="sxs-lookup"><span data-stu-id="f61e2-103">Gets an Azure Web App certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f61e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f61e2-104">SYNTAX</span></span>

```
Get-AzureRmWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f61e2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f61e2-105">DESCRIPTION</span></span>
<span data-ttu-id="f61e2-106">Cmdleten **Get-AzureRmWebAppCertificate** hämtar information om Azure Web App-certifikat som är associerade med en viss resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f61e2-106">The **Get-AzureRmWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="f61e2-107">Om du känner till tumavtryck för certifikatet kan du även använda denna cmdlet för att få information om ett visst certifikat.</span><span class="sxs-lookup"><span data-stu-id="f61e2-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="f61e2-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f61e2-108">EXAMPLES</span></span>

### <span data-ttu-id="f61e2-109">Exempel 1: Hämta webb program certifikat i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="f61e2-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="f61e2-110">Det här kommandot returnerar information om de laddade webb program certifikat som är kopplade till resurs gruppen ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f61e2-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="f61e2-111">Exempel 2: Hämta ett angivet webb program certifikat</span><span class="sxs-lookup"><span data-stu-id="f61e2-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="f61e2-112">Det här kommandot får ContosoResourceGroup-certifikatet med tumavtrycket E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span><span class="sxs-lookup"><span data-stu-id="f61e2-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="f61e2-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f61e2-113">PARAMETERS</span></span>

### <span data-ttu-id="f61e2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f61e2-114">-DefaultProfile</span></span>
<span data-ttu-id="f61e2-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f61e2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f61e2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f61e2-116">-ResourceGroupName</span></span>
<span data-ttu-id="f61e2-117">Anger namnet på resurs gruppen som certifikatet har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="f61e2-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f61e2-118">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="f61e2-118">-Thumbprint</span></span>
<span data-ttu-id="f61e2-119">Anger det unika ID: t för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="f61e2-119">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f61e2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f61e2-120">CommonParameters</span></span>
<span data-ttu-id="f61e2-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f61e2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f61e2-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f61e2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f61e2-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f61e2-123">INPUTS</span></span>

### <span data-ttu-id="f61e2-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="f61e2-124">None</span></span>
<span data-ttu-id="f61e2-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f61e2-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f61e2-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f61e2-126">OUTPUTS</span></span>

## <span data-ttu-id="f61e2-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f61e2-127">NOTES</span></span>

## <span data-ttu-id="f61e2-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f61e2-128">RELATED LINKS</span></span>

[<span data-ttu-id="f61e2-129">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="f61e2-129">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)



---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: eb1f96eaf85e6a5e7234e09c319b2e0c1117d456
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928638"
---
# <span data-ttu-id="2b1d4-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2b1d4-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="2b1d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2b1d4-102">SYNOPSIS</span></span>
<span data-ttu-id="2b1d4-103">Hämtar Azure Web Apps i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2b1d4-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b1d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2b1d4-104">SYNTAX</span></span>

### <span data-ttu-id="2b1d4-105">S</span><span class="sxs-lookup"><span data-stu-id="2b1d4-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b1d4-106">S2</span><span class="sxs-lookup"><span data-stu-id="2b1d4-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <AppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b1d4-107">S3</span><span class="sxs-lookup"><span data-stu-id="2b1d4-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b1d4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2b1d4-108">DESCRIPTION</span></span>
<span data-ttu-id="2b1d4-109">Cmdleten **Get-AzureRmWebApp** hämtar information om en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="2b1d4-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="2b1d4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2b1d4-110">EXAMPLES</span></span>

### <span data-ttu-id="2b1d4-111">Exempel 1: Hämta ett webb program från en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="2b1d4-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="2b1d4-112">Det här kommandot hämtar webb programmet som heter ContosoSite som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="2b1d4-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="2b1d4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2b1d4-113">PARAMETERS</span></span>

### <span data-ttu-id="2b1d4-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2b1d4-114">-AppServicePlan</span></span>
<span data-ttu-id="2b1d4-115">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="2b1d4-115">App Service Plan object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b1d4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b1d4-116">-DefaultProfile</span></span>
<span data-ttu-id="2b1d4-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2b1d4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b1d4-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="2b1d4-118">-Location</span></span>
<span data-ttu-id="2b1d4-119">Plats</span><span class="sxs-lookup"><span data-stu-id="2b1d4-119">Location</span></span>

```yaml
Type: String
Parameter Sets: S3
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b1d4-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="2b1d4-120">-Name</span></span>
<span data-ttu-id="2b1d4-121">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="2b1d4-121">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b1d4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b1d4-122">-ResourceGroupName</span></span>
<span data-ttu-id="2b1d4-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="2b1d4-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b1d4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b1d4-124">CommonParameters</span></span>
<span data-ttu-id="2b1d4-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b1d4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b1d4-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b1d4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b1d4-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2b1d4-127">INPUTS</span></span>

### <span data-ttu-id="2b1d4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2b1d4-128">System.String</span></span>

## <span data-ttu-id="2b1d4-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2b1d4-129">OUTPUTS</span></span>

### <span data-ttu-id="2b1d4-130">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="2b1d4-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="2b1d4-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2b1d4-131">NOTES</span></span>

## <span data-ttu-id="2b1d4-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2b1d4-132">RELATED LINKS</span></span>

[<span data-ttu-id="2b1d4-133">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2b1d4-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="2b1d4-134">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2b1d4-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="2b1d4-135">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2b1d4-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="2b1d4-136">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2b1d4-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="2b1d4-137">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2b1d4-137">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: 7dc1d2c5d6be1fd920ec9fb4eb90bf73b2c464b9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260854"
---
# <span data-ttu-id="55cb1-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="55cb1-101">Get-AzWebApp</span></span>

## <span data-ttu-id="55cb1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="55cb1-102">SYNOPSIS</span></span>
<span data-ttu-id="55cb1-103">Hämtar Azure Web Apps i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="55cb1-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="55cb1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="55cb1-104">SYNTAX</span></span>

### <span data-ttu-id="55cb1-105">S</span><span class="sxs-lookup"><span data-stu-id="55cb1-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="55cb1-106">S2</span><span class="sxs-lookup"><span data-stu-id="55cb1-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="55cb1-107">S3</span><span class="sxs-lookup"><span data-stu-id="55cb1-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55cb1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="55cb1-108">DESCRIPTION</span></span>
<span data-ttu-id="55cb1-109">Cmdleten **Get-AzWebApp** hämtar information om en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="55cb1-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="55cb1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="55cb1-110">EXAMPLES</span></span>

### <span data-ttu-id="55cb1-111">Exempel 1: Hämta ett webb program från en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="55cb1-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="55cb1-112">Det här kommandot hämtar webb programmet som heter ContosoSite som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="55cb1-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="55cb1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="55cb1-113">PARAMETERS</span></span>

### <span data-ttu-id="55cb1-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="55cb1-114">-AppServicePlan</span></span>
<span data-ttu-id="55cb1-115">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="55cb1-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55cb1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55cb1-116">-DefaultProfile</span></span>
<span data-ttu-id="55cb1-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="55cb1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55cb1-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="55cb1-118">-Location</span></span>
<span data-ttu-id="55cb1-119">Plats</span><span class="sxs-lookup"><span data-stu-id="55cb1-119">Location</span></span>

```yaml
Type: System.String
Parameter Sets: S3
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55cb1-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="55cb1-120">-Name</span></span>
<span data-ttu-id="55cb1-121">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="55cb1-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55cb1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55cb1-122">-ResourceGroupName</span></span>
<span data-ttu-id="55cb1-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="55cb1-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55cb1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55cb1-124">CommonParameters</span></span>
<span data-ttu-id="55cb1-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55cb1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55cb1-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55cb1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55cb1-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="55cb1-127">INPUTS</span></span>

### <span data-ttu-id="55cb1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="55cb1-128">System.String</span></span>

## <span data-ttu-id="55cb1-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="55cb1-129">OUTPUTS</span></span>

### <span data-ttu-id="55cb1-130">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="55cb1-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="55cb1-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="55cb1-131">NOTES</span></span>

## <span data-ttu-id="55cb1-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="55cb1-132">RELATED LINKS</span></span>

[<span data-ttu-id="55cb1-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="55cb1-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="55cb1-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="55cb1-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="55cb1-135">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="55cb1-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="55cb1-136">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="55cb1-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="55cb1-137">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="55cb1-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)



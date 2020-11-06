---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
ms.openlocfilehash: 841cc1f8356d9b082dec55e689033c19343041d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575747"
---
# <span data-ttu-id="c2182-101">Get-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c2182-101">Get-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="c2182-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2182-102">SYNOPSIS</span></span>
<span data-ttu-id="c2182-103">Hämtar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="c2182-103">Gets an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2182-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2182-104">SYNTAX</span></span>

### <span data-ttu-id="c2182-105">S</span><span class="sxs-lookup"><span data-stu-id="c2182-105">S1</span></span>
```
Get-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2182-106">S2</span><span class="sxs-lookup"><span data-stu-id="c2182-106">S2</span></span>
```
Get-AzureRmWebAppSlot [[-Slot] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2182-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2182-107">DESCRIPTION</span></span>
<span data-ttu-id="c2182-108">Cmdleten **Get-AzureRmWebAppSlot** hämtar information om en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="c2182-108">The **Get-AzureRmWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="c2182-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2182-109">EXAMPLES</span></span>

### <span data-ttu-id="c2182-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c2182-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="c2182-111">Med det här kommandot får du den plats som heter Slot001 från webb programmet som heter WebAppStandard som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="c2182-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="c2182-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2182-112">PARAMETERS</span></span>

### <span data-ttu-id="c2182-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="c2182-113">-Name</span></span>
<span data-ttu-id="c2182-114">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="c2182-114">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2182-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2182-115">-ResourceGroupName</span></span>
<span data-ttu-id="c2182-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c2182-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2182-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="c2182-117">-Slot</span></span>
<span data-ttu-id="c2182-118">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="c2182-118">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2182-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c2182-119">-WebApp</span></span>
<span data-ttu-id="c2182-120">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="c2182-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2182-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2182-121">-DefaultProfile</span></span>
<span data-ttu-id="c2182-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2182-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2182-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2182-123">CommonParameters</span></span>
<span data-ttu-id="c2182-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2182-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2182-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2182-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2182-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2182-126">INPUTS</span></span>

### <span data-ttu-id="c2182-127">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="c2182-127">Site</span></span>
<span data-ttu-id="c2182-128">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c2182-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="c2182-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2182-129">OUTPUTS</span></span>

## <span data-ttu-id="c2182-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2182-130">NOTES</span></span>

## <span data-ttu-id="c2182-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2182-131">RELATED LINKS</span></span>

[<span data-ttu-id="c2182-132">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c2182-132">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="c2182-133">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c2182-133">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="c2182-134">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c2182-134">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="c2182-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c2182-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="c2182-136">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c2182-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="c2182-137">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c2182-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="c2182-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c2182-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

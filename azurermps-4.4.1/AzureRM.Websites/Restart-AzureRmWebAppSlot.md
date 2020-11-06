---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
ms.openlocfilehash: ace1b16bc6d89fb619daba23a214326acd8d0d24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573602"
---
# <span data-ttu-id="c4a98-101">Restart-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c4a98-101">Restart-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="c4a98-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4a98-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4a98-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4a98-103">SYNTAX</span></span>

### <span data-ttu-id="c4a98-104">S</span><span class="sxs-lookup"><span data-stu-id="c4a98-104">S1</span></span>
```
Restart-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4a98-105">S2</span><span class="sxs-lookup"><span data-stu-id="c4a98-105">S2</span></span>
```
Restart-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4a98-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4a98-106">DESCRIPTION</span></span>
<span data-ttu-id="c4a98-107">Cmdleten **restart-AzureRmWebAppSlot** stoppar och startar sedan en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="c4a98-107">The **Restart-AzureRmWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="c4a98-108">Om Web App-platsen är i ett stoppat tillstånd kan du använda Start-AzureRmWebAppSlot cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4a98-108">If the Web App Slot is in a stopped state, use the Start-AzureRmWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="c4a98-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4a98-109">EXAMPLES</span></span>

### <span data-ttu-id="c4a98-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c4a98-110">Example 1</span></span>
```
PS C:\> Restart-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="c4a98-111">Det här kommandot startar om fack Slot001 för Web App-ContosoWebApp som är kopplat till resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="c4a98-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="c4a98-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4a98-112">PARAMETERS</span></span>

### <span data-ttu-id="c4a98-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="c4a98-113">-Name</span></span>
<span data-ttu-id="c4a98-114">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="c4a98-114">WebApp Name</span></span>

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

### <span data-ttu-id="c4a98-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4a98-115">-ResourceGroupName</span></span>
<span data-ttu-id="c4a98-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c4a98-116">Resource Group Name</span></span>

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

### <span data-ttu-id="c4a98-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="c4a98-117">-Slot</span></span>
<span data-ttu-id="c4a98-118">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="c4a98-118">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a98-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c4a98-119">-WebApp</span></span>
<span data-ttu-id="c4a98-120">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="c4a98-120">WebApp Object</span></span>

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

### <span data-ttu-id="c4a98-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4a98-121">-DefaultProfile</span></span>
<span data-ttu-id="c4a98-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c4a98-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4a98-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a98-123">CommonParameters</span></span>
<span data-ttu-id="c4a98-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4a98-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a98-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4a98-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a98-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4a98-126">INPUTS</span></span>

### <span data-ttu-id="c4a98-127">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="c4a98-127">Site</span></span>
<span data-ttu-id="c4a98-128">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c4a98-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="c4a98-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4a98-129">OUTPUTS</span></span>

## <span data-ttu-id="c4a98-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4a98-130">NOTES</span></span>

## <span data-ttu-id="c4a98-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4a98-131">RELATED LINKS</span></span>

[<span data-ttu-id="c4a98-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c4a98-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="c4a98-133">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c4a98-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="c4a98-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c4a98-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="c4a98-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c4a98-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="c4a98-136">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c4a98-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="c4a98-137">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c4a98-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="c4a98-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c4a98-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
ms.openlocfilehash: 2260c631981116b8ffd185b87fba05482adc3044
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920693"
---
# <span data-ttu-id="3752b-101">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="3752b-101">Get-AzDeletedWebApp</span></span>

## <span data-ttu-id="3752b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3752b-102">SYNOPSIS</span></span>
<span data-ttu-id="3752b-103">Tar bort webb program i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="3752b-103">Gets deleted web apps in the subscription.</span></span>

## <span data-ttu-id="3752b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3752b-104">SYNTAX</span></span>

```
Get-AzDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3752b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3752b-105">DESCRIPTION</span></span>
<span data-ttu-id="3752b-106">Cmdleten **Get-AzDeletedWebApp** returnerar alla borttagna webb program i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="3752b-106">The **Get-AzDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="3752b-107">Borttagna appar kan filtreras efter resurs grupp, namn och plats.</span><span class="sxs-lookup"><span data-stu-id="3752b-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="3752b-108">Det kan finnas fler än en borttagen app med samma namn och resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="3752b-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="3752b-109">Kontrol lera DeletionTime för att skilja på borttagna appar som har samma namn.</span><span class="sxs-lookup"><span data-stu-id="3752b-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="3752b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3752b-110">EXAMPLES</span></span>

### <span data-ttu-id="3752b-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3752b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="3752b-112">Det här kommandot hämtar de borttagna apparna som heter ContosoSite som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="3752b-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="3752b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3752b-113">PARAMETERS</span></span>

### <span data-ttu-id="3752b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3752b-114">-DefaultProfile</span></span>
<span data-ttu-id="3752b-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3752b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3752b-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="3752b-116">-Location</span></span>
<span data-ttu-id="3752b-117">Platsen för den borttagna appen.</span><span class="sxs-lookup"><span data-stu-id="3752b-117">The location of the deleted app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3752b-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="3752b-118">-Name</span></span>
<span data-ttu-id="3752b-119">Namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="3752b-119">The name of the web app.</span></span>

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

### <span data-ttu-id="3752b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3752b-120">-ResourceGroupName</span></span>
<span data-ttu-id="3752b-121">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3752b-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="3752b-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="3752b-122">-Slot</span></span>
<span data-ttu-id="3752b-123">Namnet på Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="3752b-123">The name of the web app slot.</span></span>

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

### <span data-ttu-id="3752b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3752b-124">CommonParameters</span></span>
<span data-ttu-id="3752b-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3752b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3752b-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3752b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3752b-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3752b-127">INPUTS</span></span>

### <span data-ttu-id="3752b-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="3752b-128">None</span></span>

## <span data-ttu-id="3752b-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3752b-129">OUTPUTS</span></span>

### <span data-ttu-id="3752b-130">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="3752b-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="3752b-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3752b-131">NOTES</span></span>

## <span data-ttu-id="3752b-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3752b-132">RELATED LINKS</span></span>

[<span data-ttu-id="3752b-133">Återställ-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="3752b-133">Restore-AzDeletedWebApp</span></span>](./Restore-AzDeletedWebApp.md)
---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CD2274E5-B3D4-489E-B374-8B2BCC1F923E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90666be18ee3e546620d0c10386594b8ae7ec8a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099465"
---
# <span data-ttu-id="d13c5-101">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="d13c5-101">New-AzureAclConfig</span></span>

## <span data-ttu-id="d13c5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d13c5-102">SYNOPSIS</span></span>
<span data-ttu-id="d13c5-103">Skapar ett tomt ACL-konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="d13c5-103">Creates an empty ACL configuration object.</span></span>

## <span data-ttu-id="d13c5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d13c5-104">SYNTAX</span></span>

```
New-AzureAclConfig [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d13c5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d13c5-105">DESCRIPTION</span></span>
<span data-ttu-id="d13c5-106">Cmdleten **New-AzureAclConfig** skapar ett tomt ACL-konfigurationsobjekt (Access Control List).</span><span class="sxs-lookup"><span data-stu-id="d13c5-106">The **New-AzureAclConfig** cmdlet creates an empty access control list (ACL) configuration object.</span></span>

## <span data-ttu-id="d13c5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d13c5-107">EXAMPLES</span></span>

### <span data-ttu-id="d13c5-108">Exempel 1: skapa en ACL-konfigurationsfil</span><span class="sxs-lookup"><span data-stu-id="d13c5-108">Example 1: Create an ACL configuration object</span></span>
```
PS C:\> $Acl = New-AzureAclConfig
```

<span data-ttu-id="d13c5-109">Det här kommandot skapar ett tomt ACL-konfigurationsobjekt och lagrar det sedan i $Acl variabel.</span><span class="sxs-lookup"><span data-stu-id="d13c5-109">This command creates an empty ACL configuration object, and then stores it in the $Acl variable.</span></span>

## <span data-ttu-id="d13c5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d13c5-110">PARAMETERS</span></span>

### <span data-ttu-id="d13c5-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d13c5-111">-InformationAction</span></span>
<span data-ttu-id="d13c5-112">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="d13c5-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d13c5-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d13c5-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d13c5-114">Vidare</span><span class="sxs-lookup"><span data-stu-id="d13c5-114">Continue</span></span>
- <span data-ttu-id="d13c5-115">Över</span><span class="sxs-lookup"><span data-stu-id="d13c5-115">Ignore</span></span>
- <span data-ttu-id="d13c5-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="d13c5-116">Inquire</span></span>
- <span data-ttu-id="d13c5-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d13c5-117">SilentlyContinue</span></span>
- <span data-ttu-id="d13c5-118">Stanna</span><span class="sxs-lookup"><span data-stu-id="d13c5-118">Stop</span></span>
- <span data-ttu-id="d13c5-119">Avbryt</span><span class="sxs-lookup"><span data-stu-id="d13c5-119">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d13c5-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d13c5-120">-InformationVariable</span></span>
<span data-ttu-id="d13c5-121">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="d13c5-121">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d13c5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d13c5-122">CommonParameters</span></span>
<span data-ttu-id="d13c5-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d13c5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d13c5-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d13c5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d13c5-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d13c5-125">INPUTS</span></span>

## <span data-ttu-id="d13c5-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d13c5-126">OUTPUTS</span></span>

## <span data-ttu-id="d13c5-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d13c5-127">NOTES</span></span>

## <span data-ttu-id="d13c5-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d13c5-128">RELATED LINKS</span></span>

[<span data-ttu-id="d13c5-129">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="d13c5-129">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="d13c5-130">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="d13c5-130">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="d13c5-131">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="d13c5-131">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)



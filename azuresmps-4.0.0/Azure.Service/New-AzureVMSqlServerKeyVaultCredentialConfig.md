---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EC6F7790-5E31-4C22-B006-38B5C1868671
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0272740ced33d19e2610a6116812df4a815ea3c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099418"
---
# <span data-ttu-id="ba704-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="ba704-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="ba704-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ba704-102">SYNOPSIS</span></span>

## <span data-ttu-id="ba704-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ba704-103">SYNTAX</span></span>

```
New-AzureVMSqlServerKeyVaultCredentialConfig [-Enable] [[-CredentialName] <String>]
 [[-AzureKeyVaultUrl] <String>] [[-ServicePrincipalName] <String>] [[-ServicePrincipalSecret] <SecureString>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba704-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ba704-104">DESCRIPTION</span></span>

## <span data-ttu-id="ba704-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ba704-105">EXAMPLES</span></span>

### <span data-ttu-id="ba704-106">9.1</span><span class="sxs-lookup"><span data-stu-id="ba704-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="ba704-107">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ba704-107">PARAMETERS</span></span>

### <span data-ttu-id="ba704-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="ba704-108">-AzureKeyVaultUrl</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba704-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="ba704-109">-CredentialName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba704-110">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="ba704-110">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba704-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ba704-111">-InformationAction</span></span>
<span data-ttu-id="ba704-112">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="ba704-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ba704-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ba704-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ba704-114">Vidare</span><span class="sxs-lookup"><span data-stu-id="ba704-114">Continue</span></span>
- <span data-ttu-id="ba704-115">Över</span><span class="sxs-lookup"><span data-stu-id="ba704-115">Ignore</span></span>
- <span data-ttu-id="ba704-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="ba704-116">Inquire</span></span>
- <span data-ttu-id="ba704-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ba704-117">SilentlyContinue</span></span>
- <span data-ttu-id="ba704-118">Stanna</span><span class="sxs-lookup"><span data-stu-id="ba704-118">Stop</span></span>
- <span data-ttu-id="ba704-119">Avbryt</span><span class="sxs-lookup"><span data-stu-id="ba704-119">Suspend</span></span>

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

### <span data-ttu-id="ba704-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ba704-120">-InformationVariable</span></span>
<span data-ttu-id="ba704-121">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="ba704-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ba704-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="ba704-122">-Profile</span></span>
```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba704-123">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ba704-123">-ServicePrincipalName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba704-124">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="ba704-124">-ServicePrincipalSecret</span></span>
```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba704-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba704-125">CommonParameters</span></span>
<span data-ttu-id="ba704-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba704-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba704-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba704-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba704-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ba704-128">INPUTS</span></span>

## <span data-ttu-id="ba704-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ba704-129">OUTPUTS</span></span>

## <span data-ttu-id="ba704-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ba704-130">NOTES</span></span>

## <span data-ttu-id="ba704-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ba704-131">RELATED LINKS</span></span>


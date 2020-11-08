---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C69558DB-78C3-4162-99C3-1300C3FE5287
online version: ''
schema: 2.0.0
ms.openlocfilehash: aa73cf467ffc3675b17b6c59ef5bd07483803267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093385"
---
# <span data-ttu-id="1acec-101">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="1acec-101">Get-AzureAutomationCredential</span></span>

## <span data-ttu-id="1acec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1acec-102">SYNOPSIS</span></span>

<span data-ttu-id="1acec-103">Hämtar en Azure Automation-autentiseringsuppgift.</span><span class="sxs-lookup"><span data-stu-id="1acec-103">Gets an Azure Automation credential.</span></span>

## <span data-ttu-id="1acec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1acec-104">SYNTAX</span></span>

### <span data-ttu-id="1acec-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="1acec-105">ByAll (Default)</span></span>
```
Get-AzureAutomationCredential -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1acec-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1acec-106">ByName</span></span>
```
Get-AzureAutomationCredential -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1acec-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1acec-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="1acec-108">Cmdleten **Get-AzureAutomationCredential** hämtar en eller flera Microsoft Azure Automation-uppgifter.</span><span class="sxs-lookup"><span data-stu-id="1acec-108">The **Get-AzureAutomationCredential** cmdlet gets one or more Microsoft Azure Automation credentials.</span></span>
<span data-ttu-id="1acec-109">Som standard returneras alla autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="1acec-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="1acec-110">Ange namnet på en viss autentiseringsuppgift.</span><span class="sxs-lookup"><span data-stu-id="1acec-110">To get a specific credential, specify its name.</span></span>

## <span data-ttu-id="1acec-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1acec-111">EXAMPLES</span></span>

### <span data-ttu-id="1acec-112">Exempel 1: Hämta alla autentiseringsuppgifter</span><span class="sxs-lookup"><span data-stu-id="1acec-112">Example 1: Get all credentials</span></span>
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17"
```

<span data-ttu-id="1acec-113">Det här kommandot får alla autentiseringsuppgifter i Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="1acec-113">This command gets all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="1acec-114">Exempel 2: skaffa en autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="1acec-114">Example 2: Get a credential</span></span>
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential"
```

<span data-ttu-id="1acec-115">Det här kommandot får autentiseringsuppgiften med namnet mina autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="1acec-115">This command gets the credential named MyCredential.</span></span>

## <span data-ttu-id="1acec-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1acec-116">PARAMETERS</span></span>

### <span data-ttu-id="1acec-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1acec-117">-AutomationAccountName</span></span>
<span data-ttu-id="1acec-118">Anger namnet på Automation-kontot med autentiseringsuppgiften som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="1acec-118">Specifies the name of the automation account with the credential to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1acec-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="1acec-119">-Name</span></span>
<span data-ttu-id="1acec-120">Anger namnet på en autentiseringsuppgift som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="1acec-120">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1acec-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="1acec-121">-Profile</span></span>
<span data-ttu-id="1acec-122">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="1acec-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1acec-123">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="1acec-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1acec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1acec-124">CommonParameters</span></span>
<span data-ttu-id="1acec-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1acec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1acec-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1acec-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1acec-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1acec-127">INPUTS</span></span>

## <span data-ttu-id="1acec-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1acec-128">OUTPUTS</span></span>

### <span data-ttu-id="1acec-129">Microsoft. Azure. commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="1acec-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="1acec-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1acec-130">NOTES</span></span>

## <span data-ttu-id="1acec-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1acec-131">RELATED LINKS</span></span>

[<span data-ttu-id="1acec-132">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="1acec-132">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="1acec-133">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="1acec-133">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)

[<span data-ttu-id="1acec-134">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="1acec-134">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)



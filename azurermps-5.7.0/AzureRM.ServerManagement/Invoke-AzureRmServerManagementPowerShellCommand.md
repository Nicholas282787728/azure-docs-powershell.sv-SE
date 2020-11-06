---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1EA5F348-5EF4-4056-BA06-7B95E12E329D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/invoke-azurermservermanagementpowershellcommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
ms.openlocfilehash: d4720a1159d55064a007a97df7233853200f1295
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575513"
---
# <span data-ttu-id="3ad48-101">Invoke-AzureRmServerManagementPowerShellCommand</span><span class="sxs-lookup"><span data-stu-id="3ad48-101">Invoke-AzureRmServerManagementPowerShellCommand</span></span>

## <span data-ttu-id="3ad48-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ad48-102">SYNOPSIS</span></span>
<span data-ttu-id="3ad48-103">Kör ett skript block för Windows PowerShell på en nod.</span><span class="sxs-lookup"><span data-stu-id="3ad48-103">Executes a Windows PowerShell script block on a node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ad48-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ad48-104">SYNTAX</span></span>

### <span data-ttu-id="3ad48-105">ByName</span><span class="sxs-lookup"><span data-stu-id="3ad48-105">ByName</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-Command] <ScriptBlock> [-PowerShellSessionName <String>] [-RawOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ad48-106">BySession</span><span class="sxs-lookup"><span data-stu-id="3ad48-106">BySession</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-Session] <Session> [-Command] <ScriptBlock>
 [-PowerShellSessionName <String>] [-RawOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ad48-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ad48-107">DESCRIPTION</span></span>
<span data-ttu-id="3ad48-108">Cmdleten **Invoke-AzureRmServerManagementPowerShellCommand** kör ett skript block för Windows PowerShell på en nod som hanteras av en Azure Server Management Gateway.</span><span class="sxs-lookup"><span data-stu-id="3ad48-108">The **Invoke-AzureRmServerManagementPowerShellCommand** cmdlet executes a Windows PowerShell script block on a node managed by an Azure Server Management Gateway.</span></span>

## <span data-ttu-id="3ad48-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ad48-109">EXAMPLES</span></span>

## <span data-ttu-id="3ad48-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ad48-110">PARAMETERS</span></span>

### <span data-ttu-id="3ad48-111">-Kommando</span><span class="sxs-lookup"><span data-stu-id="3ad48-111">-Command</span></span>
<span data-ttu-id="3ad48-112">Anger det skript block som ska köras på målnoden.</span><span class="sxs-lookup"><span data-stu-id="3ad48-112">Specifies the script block to run on the target node.</span></span>

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ad48-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ad48-113">-DefaultProfile</span></span>
<span data-ttu-id="3ad48-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3ad48-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ad48-115">-Nodnamn</span><span class="sxs-lookup"><span data-stu-id="3ad48-115">-NodeName</span></span>
<span data-ttu-id="3ad48-116">Anger namnet på den nod som skript blocket ska köras på.</span><span class="sxs-lookup"><span data-stu-id="3ad48-116">Specifies the name of the node to run the script block on.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ad48-117">-PowerShellSessionName</span><span class="sxs-lookup"><span data-stu-id="3ad48-117">-PowerShellSessionName</span></span>
<span data-ttu-id="3ad48-118">Anger namnet på Windows PowerShell-startsidan på målnoden.</span><span class="sxs-lookup"><span data-stu-id="3ad48-118">Specifies the name of the Windows PowerShell run space on the target node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ad48-119">-RawOutput</span><span class="sxs-lookup"><span data-stu-id="3ad48-119">-RawOutput</span></span>
<span data-ttu-id="3ad48-120">Anger att cmdleten returnerar det fullständiga objekt som innehåller utdata från noden.</span><span class="sxs-lookup"><span data-stu-id="3ad48-120">Indicates that the cmdlet returns the complete object that contains the output from the node.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ad48-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ad48-121">-ResourceGroupName</span></span>
<span data-ttu-id="3ad48-122">Anger namnet på den resurs grupp som noden tillhör.</span><span class="sxs-lookup"><span data-stu-id="3ad48-122">Specifies the name of the resource group that the node belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ad48-123">-Session</span><span class="sxs-lookup"><span data-stu-id="3ad48-123">-Session</span></span>
<span data-ttu-id="3ad48-124">Anger det **session** -objekt som denna cmdlet använder för att ansluta till målnoden.</span><span class="sxs-lookup"><span data-stu-id="3ad48-124">Specifies the **Session** object that this cmdlet uses to connect to the target node.</span></span>

<span data-ttu-id="3ad48-125">Den här parametern kan anges i stället för parametrarna *ResourceGroupName* , *nodnamn* , *sessionname* och *PowerShellSessionName* .</span><span class="sxs-lookup"><span data-stu-id="3ad48-125">This parameter may be specified instead of the *ResourceGroupName* , *NodeName* , *SessionName* , and *PowerShellSessionName* parameters.</span></span>

```yaml
Type: Session
Parameter Sets: BySession
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ad48-126">-Sessionsnamn</span><span class="sxs-lookup"><span data-stu-id="3ad48-126">-SessionName</span></span>
<span data-ttu-id="3ad48-127">Anger namnet på den session som ska hantera noden.</span><span class="sxs-lookup"><span data-stu-id="3ad48-127">Specifies the name of the session to manage the node.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ad48-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ad48-128">CommonParameters</span></span>
<span data-ttu-id="3ad48-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ad48-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ad48-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ad48-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ad48-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ad48-131">INPUTS</span></span>

### <span data-ttu-id="3ad48-132">Dialogsessionen</span><span class="sxs-lookup"><span data-stu-id="3ad48-132">Session</span></span>
<span data-ttu-id="3ad48-133">Parametern ' session ' godkänner värdet för typen session från pipeline</span><span class="sxs-lookup"><span data-stu-id="3ad48-133">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="3ad48-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ad48-134">OUTPUTS</span></span>

### <span data-ttu-id="3ad48-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="3ad48-135">System.Object</span></span>

## <span data-ttu-id="3ad48-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ad48-136">NOTES</span></span>

## <span data-ttu-id="3ad48-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ad48-137">RELATED LINKS</span></span>

[<span data-ttu-id="3ad48-138">Azure Server Management-cmdletar</span><span class="sxs-lookup"><span data-stu-id="3ad48-138">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
ms.openlocfilehash: 244adfb2707d47cef56390ce0d707b9f51fe229b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261550"
---
# <span data-ttu-id="bd0c7-101">New-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="bd0c7-101">New-AzStackEdgeUser</span></span>

## <span data-ttu-id="bd0c7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd0c7-102">SYNOPSIS</span></span>
<span data-ttu-id="bd0c7-103">Skapar en ny användare för enheten.</span><span class="sxs-lookup"><span data-stu-id="bd0c7-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="bd0c7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd0c7-104">SYNTAX</span></span>

```
New-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd0c7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd0c7-105">DESCRIPTION</span></span>
<span data-ttu-id="bd0c7-106">Cmdleten **New-AzStackEdgeUser** skapar en ny användare för Travan.</span><span class="sxs-lookup"><span data-stu-id="bd0c7-106">The **New-AzStackEdgeUser** cmdlet creates a new user for the Stack Edge device.</span></span> <span data-ttu-id="bd0c7-107">Det går bara att skapa en typ av användare `Share` .</span><span class="sxs-lookup"><span data-stu-id="bd0c7-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="bd0c7-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd0c7-108">EXAMPLES</span></span>

### <span data-ttu-id="bd0c7-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bd0c7-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="bd0c7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd0c7-110">PARAMETERS</span></span>

### <span data-ttu-id="bd0c7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd0c7-111">-AsJob</span></span>
<span data-ttu-id="bd0c7-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="bd0c7-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd0c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd0c7-113">-DefaultProfile</span></span>
<span data-ttu-id="bd0c7-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bd0c7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd0c7-115">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="bd0c7-115">-DeviceName</span></span>
<span data-ttu-id="bd0c7-116">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="bd0c7-116">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0c7-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="bd0c7-117">-EncryptionKey</span></span>
<span data-ttu-id="bd0c7-118">Enhetens krypterings nycklar</span><span class="sxs-lookup"><span data-stu-id="bd0c7-118">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd0c7-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="bd0c7-119">-Name</span></span>
<span data-ttu-id="bd0c7-120">Namnen</span><span class="sxs-lookup"><span data-stu-id="bd0c7-120">Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0c7-121">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="bd0c7-121">-Password</span></span>
<span data-ttu-id="bd0c7-122">Lösen ord, ange som en säker sträng</span><span class="sxs-lookup"><span data-stu-id="bd0c7-122">Password, provide as a secure string</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd0c7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd0c7-123">-ResourceGroupName</span></span>
<span data-ttu-id="bd0c7-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="bd0c7-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0c7-125">– Skriv</span><span class="sxs-lookup"><span data-stu-id="bd0c7-125">-Type</span></span>
<span data-ttu-id="bd0c7-126">Välj UserType</span><span class="sxs-lookup"><span data-stu-id="bd0c7-126">Select UserType</span></span>

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

### <span data-ttu-id="bd0c7-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bd0c7-127">-Confirm</span></span>
<span data-ttu-id="bd0c7-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bd0c7-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd0c7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd0c7-129">-WhatIf</span></span>
<span data-ttu-id="bd0c7-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bd0c7-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd0c7-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bd0c7-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd0c7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd0c7-132">CommonParameters</span></span>
<span data-ttu-id="bd0c7-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd0c7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd0c7-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd0c7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd0c7-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd0c7-135">INPUTS</span></span>

### <span data-ttu-id="bd0c7-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="bd0c7-136">None</span></span>

## <span data-ttu-id="bd0c7-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd0c7-137">OUTPUTS</span></span>

### <span data-ttu-id="bd0c7-138">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="bd0c7-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="bd0c7-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd0c7-139">NOTES</span></span>

## <span data-ttu-id="bd0c7-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd0c7-140">RELATED LINKS</span></span>
---
title: 規則運算式 2 語法
ms.author: comanea
author: dan-wesley
manager: seanlyn
ms.date: 06/09/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 規則運算式 2 語法
ms.openlocfilehash: 5d7026a034300e098497c63911f7516f72877c5d
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617313"
---
# <a name="regular-expression-2-re2h-syntax"></a><span data-ttu-id="32656-103">規則運算式 2 (re2.h) 語法</span><span class="sxs-lookup"><span data-stu-id="32656-103">Regular Expression 2 (re2.h) syntax</span></span>

<span data-ttu-id="32656-104">規則運算式是描述字元字串集的標記法。</span><span class="sxs-lookup"><span data-stu-id="32656-104">Regular expressions are a notation for describing sets of character strings.</span></span> <span data-ttu-id="32656-105">如果字串位於規則運算式所描述的集中，我們通常表示規則運算式與字串相符。</span><span class="sxs-lookup"><span data-stu-id="32656-105">When a string is in the set described by a regular expression, we often say that the regular expression matches the string.</span></span>

<span data-ttu-id="32656-106">最簡單的規則運算式是單一常值字元。</span><span class="sxs-lookup"><span data-stu-id="32656-106">The simplest regular expression is a single literal character.</span></span> <span data-ttu-id="32656-107">除*\*+?()|* 以外的元字元，字元與其本身相符。</span><span class="sxs-lookup"><span data-stu-id="32656-107">Except for the metacharacters like *\*+?()|*, characters match themselves.</span></span> <span data-ttu-id="32656-108">若要與元字元相符，請以反斜線將它轉義：\+ 符合常值加字元。</span><span class="sxs-lookup"><span data-stu-id="32656-108">To match a metacharacter, escape it with a backslash: \+ matches a literal plus character.</span></span>

<span data-ttu-id="32656-109">可以變更或串連兩個規則運算式，以形成新規則運算式：如果 *e<sub>1</sub>* 符合 _s_ 和*e<sub>2</sub>* 符合 _t_，則*<sub>1</sub>*  | *e<sub>2</sub> *符合 _s_ 或 _t_，以及*e<sub>1</sub>* *e<sub>2</sub>* 符合__ st。</span><span class="sxs-lookup"><span data-stu-id="32656-109">Two regular expressions can be altered or concatenated to form a new regular expression: if *e<sub>1</sub>* matches _s_ and *e<sub>2</sub>* matches _t_, then *e<sub>1</sub>* | *e<sub>2</sub>* matches _s_ or _t_, and *e<sub>1</sub>* *e<sub>2</sub>*  matches _st_.</span></span>

<span data-ttu-id="32656-110">元字元_\*_、_+_，以及 _？_</span><span class="sxs-lookup"><span data-stu-id="32656-110">The metacharacters _\*_ , _+_ , and _?_</span></span> <span data-ttu-id="32656-111">是重複運算子：*e<sub>1</sub>* _\*_ 與零個或多個 (可能不同的) 字串順序相符，其中每個字串都符合 *e<sub>1</sub>*；*e<sub>1</sub>* _+_ 符合一或多個；*e<sub>1</sub>* _？_</span><span class="sxs-lookup"><span data-stu-id="32656-111">are repetition operators: *e<sub>1</sub>* _\*_ matches a sequence of zero or more (possibly different) strings, each of which match *e<sub>1</sub>*; *e<sub>1</sub>* _+_ matches one or more; *e<sub>1</sub>* _?_</span></span> <span data-ttu-id="32656-112">符合零或一。</span><span class="sxs-lookup"><span data-stu-id="32656-112">matches zero or one.</span></span>

<span data-ttu-id="32656-113">運算子的優先順序 (從最弱到最强的繫結)，首先是替代，然後是串連，最後是重複運算子。</span><span class="sxs-lookup"><span data-stu-id="32656-113">The operator precedence, from weakest to strongest binding, is first alternation, then concatenation, and finally the repetition operators.</span></span> <span data-ttu-id="32656-114">顯式括弧可以用於強制不同的意義，就像在算術運算式中一樣。</span><span class="sxs-lookup"><span data-stu-id="32656-114">Explicit parentheses can be used to force different meanings, just as in arithmetic expressions.</span></span> <span data-ttu-id="32656-115">一些範例：_ab|cd_ 等同于_ (ab)|(cd)_ ； _ab\*_ 等同于 _a(b\*)_ 。</span><span class="sxs-lookup"><span data-stu-id="32656-115">Some examples: _ab|cd_ is equivalent to _(ab)|(cd)_ ; _ab\*_ is equivalent to _a(b\*)_ .</span></span>

<span data-ttu-id="32656-116">到目前為止描述的語法是大多數傳統的 Unix _egrep_ 規則運算式語法。</span><span class="sxs-lookup"><span data-stu-id="32656-116">The syntax described so far is most of the traditional Unix _egrep_ regular expression syntax.</span></span> <span data-ttu-id="32656-117">這個子集足以描述所有的常規語言：不嚴格地說，規則語言是一組字串，這些字串只需使用固定的記憶體量就可以在一次通過文字時進行匹配。</span><span class="sxs-lookup"><span data-stu-id="32656-117">This subset suffices to describe all regular languages: loosely speaking, a regular language is a set of strings that can be matched in a single pass through the text using only a fixed amount of memory.</span></span> <span data-ttu-id="32656-118">較新的規則運算式設備 (特別是 Perl 和那些複製它的設備) 新增了許多新的運算子和逸出序列，這使得規則運算式更簡潔，有時更神秘，但通常不是更强大。</span><span class="sxs-lookup"><span data-stu-id="32656-118">Newer regular expression facilities (notably Perl and those that have copied it) have added many new operators and escape sequences, which make the regular expressions more concise, and sometimes more cryptic, but usually not more powerful.</span></span>

<span data-ttu-id="32656-119">此頁面列出了 RE2 接受的規則運算式語法。</span><span class="sxs-lookup"><span data-stu-id="32656-119">This page lists the regular expression syntax accepted by RE2.</span></span>

<span data-ttu-id="32656-120">它也列出了一些 PCRE、PERL 和 VIM 接受的語法。</span><span class="sxs-lookup"><span data-stu-id="32656-120">It also lists some syntax accepted by PCRE, PERL and VIM.</span></span>

## <a name="syntax-tables"></a><span data-ttu-id="32656-121">語法資料表</span><span class="sxs-lookup"><span data-stu-id="32656-121">Syntax tables</span></span>

| <span data-ttu-id="32656-122">各種單字元運算式</span><span class="sxs-lookup"><span data-stu-id="32656-122">Kinds of single-character expressions</span></span> | <span data-ttu-id="32656-123">範例</span><span class="sxs-lookup"><span data-stu-id="32656-123">Examples</span></span> |
| --- | --- |
| <span data-ttu-id="32656-124">任何字元，可能包括新行字元 (s=true)</span><span class="sxs-lookup"><span data-stu-id="32656-124">any character, possibly including newline (s=true)</span></span> | <span data-ttu-id="32656-125">.</span><span class="sxs-lookup"><span data-stu-id="32656-125">.</span></span> |
| <span data-ttu-id="32656-126">字元類別</span><span class="sxs-lookup"><span data-stu-id="32656-126">character class</span></span> | <span data-ttu-id="32656-127">[xyz]</span><span class="sxs-lookup"><span data-stu-id="32656-127">[xyz]</span></span> |
| <span data-ttu-id="32656-128">反字元類別</span><span class="sxs-lookup"><span data-stu-id="32656-128">negated character class</span></span> | <span data-ttu-id="32656-129">[^xyz]</span><span class="sxs-lookup"><span data-stu-id="32656-129">[^xyz]</span></span> |
| <span data-ttu-id="32656-130">Perl 字元類別 ([連結](#user-content-perl))</span><span class="sxs-lookup"><span data-stu-id="32656-130">Perl character class ([link](#user-content-perl))</span></span> | <span data-ttu-id="32656-131">\d</span><span class="sxs-lookup"><span data-stu-id="32656-131">\d</span></span> |
| <span data-ttu-id="32656-132">反 Perl 字元類別</span><span class="sxs-lookup"><span data-stu-id="32656-132">negated Perl character class</span></span> | <span data-ttu-id="32656-133">\D</span><span class="sxs-lookup"><span data-stu-id="32656-133">\D</span></span> |
| <span data-ttu-id="32656-134">ASCII 字元類別 ([連結](#user-content-ascii))</span><span class="sxs-lookup"><span data-stu-id="32656-134">ASCII character class ([link](#user-content-ascii))</span></span> | <span data-ttu-id="32656-135">[[:alpha:]]</span><span class="sxs-lookup"><span data-stu-id="32656-135">[[:alpha:]]</span></span> |
| <span data-ttu-id="32656-136">反 ASCII 字元類別</span><span class="sxs-lookup"><span data-stu-id="32656-136">negated ASCII character class</span></span> | <span data-ttu-id="32656-137">[[:^alpha:]]</span><span class="sxs-lookup"><span data-stu-id="32656-137">[[:^alpha:]]</span></span> |
| <span data-ttu-id="32656-138">Unicode 字元類別 (單字母名稱)</span><span class="sxs-lookup"><span data-stu-id="32656-138">Unicode character class (one-letter name)</span></span> | <span data-ttu-id="32656-139">\pN</span><span class="sxs-lookup"><span data-stu-id="32656-139">\pN</span></span> |
| <span data-ttu-id="32656-140">Unicode 字元類別</span><span class="sxs-lookup"><span data-stu-id="32656-140">Unicode character class</span></span> | <span data-ttu-id="32656-141">\p{Greek}</span><span class="sxs-lookup"><span data-stu-id="32656-141">\p{Greek}</span></span> |
| <span data-ttu-id="32656-142">反 Unicode 字元類 (單字母名稱)</span><span class="sxs-lookup"><span data-stu-id="32656-142">negated Unicode character class (one-letter name)</span></span> | <span data-ttu-id="32656-143">\PN</span><span class="sxs-lookup"><span data-stu-id="32656-143">\PN</span></span> |
| <span data-ttu-id="32656-144">反 Unicode 字元類別</span><span class="sxs-lookup"><span data-stu-id="32656-144">negated Unicode character class</span></span> | <span data-ttu-id="32656-145">\P{Greek}</span><span class="sxs-lookup"><span data-stu-id="32656-145">\P{Greek}</span></span> |

|&nbsp;| <span data-ttu-id="32656-146">複合</span><span class="sxs-lookup"><span data-stu-id="32656-146">Composites</span></span> |
| --- | --- |
| <span data-ttu-id="32656-147">xy</span><span class="sxs-lookup"><span data-stu-id="32656-147">xy</span></span> | <span data-ttu-id="32656-148">x 後接 y</span><span class="sxs-lookup"><span data-stu-id="32656-148">x followed by y</span></span> |
| <span data-ttu-id="32656-149">x\|y</span><span class="sxs-lookup"><span data-stu-id="32656-149">x\|y</span></span> | <span data-ttu-id="32656-150">x 或 y (偏好 x)</span><span class="sxs-lookup"><span data-stu-id="32656-150">x or y (prefer x)</span></span> |

|&nbsp;| <span data-ttu-id="32656-151">重複</span><span class="sxs-lookup"><span data-stu-id="32656-151">Repetitions</span></span> |
| --- | --- |
| <span data-ttu-id="32656-152">x\*</span><span class="sxs-lookup"><span data-stu-id="32656-152">x\*</span></span> | <span data-ttu-id="32656-153">零或多個 x，偏好更多</span><span class="sxs-lookup"><span data-stu-id="32656-153">zero or more x, prefer more</span></span> |
| <span data-ttu-id="32656-154">x+</span><span class="sxs-lookup"><span data-stu-id="32656-154">x+</span></span> | <span data-ttu-id="32656-155">一個或多個 x，偏好更多</span><span class="sxs-lookup"><span data-stu-id="32656-155">one or more x, prefer more</span></span> |
| <span data-ttu-id="32656-156">x?</span><span class="sxs-lookup"><span data-stu-id="32656-156">x?</span></span> | <span data-ttu-id="32656-157">零或一個 x，偏好更多</span><span class="sxs-lookup"><span data-stu-id="32656-157">zero or one x, prefer one</span></span> |
| <span data-ttu-id="32656-158">x{n,m}</span><span class="sxs-lookup"><span data-stu-id="32656-158">x{n,m}</span></span> | <span data-ttu-id="32656-159">n 或 n+1 或 ... 或 m x，偏好更多</span><span class="sxs-lookup"><span data-stu-id="32656-159">n or n+1 or ... or m x, prefer more</span></span> |
| <span data-ttu-id="32656-160">x{n,}</span><span class="sxs-lookup"><span data-stu-id="32656-160">x{n,}</span></span> | <span data-ttu-id="32656-161">n 或更多 x，偏好更多</span><span class="sxs-lookup"><span data-stu-id="32656-161">n or more x, prefer more</span></span> |
| <span data-ttu-id="32656-162">x{n}</span><span class="sxs-lookup"><span data-stu-id="32656-162">x{n}</span></span> | <span data-ttu-id="32656-163">完全符合 n x</span><span class="sxs-lookup"><span data-stu-id="32656-163">exactly n x</span></span> |
| <span data-ttu-id="32656-164">x\*?</span><span class="sxs-lookup"><span data-stu-id="32656-164">x\*?</span></span> | <span data-ttu-id="32656-165">零或多個 x，偏好更少</span><span class="sxs-lookup"><span data-stu-id="32656-165">zero or more x, prefer fewer</span></span> |
| <span data-ttu-id="32656-166">x+?</span><span class="sxs-lookup"><span data-stu-id="32656-166">x+?</span></span> | <span data-ttu-id="32656-167">一個或多個 x，偏好更少</span><span class="sxs-lookup"><span data-stu-id="32656-167">one or more x, prefer fewer</span></span> |
| <span data-ttu-id="32656-168">x??</span><span class="sxs-lookup"><span data-stu-id="32656-168">x??</span></span> | <span data-ttu-id="32656-169">零或一個 x，偏好零</span><span class="sxs-lookup"><span data-stu-id="32656-169">zero or one x, prefer zero</span></span> |
| <span data-ttu-id="32656-170">x{n,m}?</span><span class="sxs-lookup"><span data-stu-id="32656-170">x{n,m}?</span></span> | <span data-ttu-id="32656-171">n 或 n+1 或 ... 或 m x，偏好更少</span><span class="sxs-lookup"><span data-stu-id="32656-171">n or n+1 or ... or m x, prefer fewer</span></span> |
| <span data-ttu-id="32656-172">x{n,}?</span><span class="sxs-lookup"><span data-stu-id="32656-172">x{n,}?</span></span> | <span data-ttu-id="32656-173">n 或更多 x，偏好更少</span><span class="sxs-lookup"><span data-stu-id="32656-173">n or more x, prefer fewer</span></span> |
| <span data-ttu-id="32656-174">x{n}?</span><span class="sxs-lookup"><span data-stu-id="32656-174">x{n}?</span></span> | <span data-ttu-id="32656-175">完全符合 n x</span><span class="sxs-lookup"><span data-stu-id="32656-175">exactly n x</span></span> |
| <span data-ttu-id="32656-176">x{}</span><span class="sxs-lookup"><span data-stu-id="32656-176">x{}</span></span> | <span data-ttu-id="32656-177">(≡ x\*) (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-177">(≡ x\*) (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-178">x{-}</span><span class="sxs-lookup"><span data-stu-id="32656-178">x{-}</span></span> | <span data-ttu-id="32656-179">(≡ x\*?) (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-179">(≡ x\*?) (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-180">x{-n}</span><span class="sxs-lookup"><span data-stu-id="32656-180">x{-n}</span></span> | <span data-ttu-id="32656-181">(≡ x{n}?) (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-181">(≡ x{n}?) (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-182">x=</span><span class="sxs-lookup"><span data-stu-id="32656-182">x=</span></span> | <span data-ttu-id="32656-183">(≡ x?) (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-183">(≡ x?) (NOT SUPPORTED) VIM</span></span> |

<span data-ttu-id="32656-184">實作限制：計算表單 x {n,m}，x {n,} 和 x {n} 拒絕創建最小或最大重複計數超過 1000 的表單。</span><span class="sxs-lookup"><span data-stu-id="32656-184">Implementation restriction: The counting forms x{n,m}, x{n,}, and x{n} reject forms that create a minimum or maximum repetition count above 1000.</span></span> <span data-ttu-id="32656-185">無限重複不受此限制。</span><span class="sxs-lookup"><span data-stu-id="32656-185">Unlimited repetitions are not subject to this restriction.</span></span>

|&nbsp;| <span data-ttu-id="32656-186">所有格重複</span><span class="sxs-lookup"><span data-stu-id="32656-186">Possessive repetitions</span></span> |
| --- | --- |
| <span data-ttu-id="32656-187">x\*+</span><span class="sxs-lookup"><span data-stu-id="32656-187">x\*+</span></span> | <span data-ttu-id="32656-188">零個或多個 x、所有格 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-188">zero or more x, possessive (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-189">x++</span><span class="sxs-lookup"><span data-stu-id="32656-189">x++</span></span> | <span data-ttu-id="32656-190">一或多個 x、所有格 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-190">one or more x, possessive (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-191">x?+</span><span class="sxs-lookup"><span data-stu-id="32656-191">x?+</span></span> | <span data-ttu-id="32656-192">零個或一個 x、所有格 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-192">zero or one x, possessive (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-193">x{n,m}+</span><span class="sxs-lookup"><span data-stu-id="32656-193">x{n,m}+</span></span> | <span data-ttu-id="32656-194">n 或 ... 或 m x，所有格 (不支持)</span><span class="sxs-lookup"><span data-stu-id="32656-194">n or ... or m x, possessive (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-195">x{n,}+</span><span class="sxs-lookup"><span data-stu-id="32656-195">x{n,}+</span></span> | <span data-ttu-id="32656-196">n 或多個 x，所有格 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-196">n or more x, possessive (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-197">x{n}+</span><span class="sxs-lookup"><span data-stu-id="32656-197">x{n}+</span></span> | <span data-ttu-id="32656-198">完全符合 n x，所有格 (不支持)</span><span class="sxs-lookup"><span data-stu-id="32656-198">exactly n x, possessive (NOT SUPPORTED)</span></span> |

|&nbsp;| <span data-ttu-id="32656-199">分組</span><span class="sxs-lookup"><span data-stu-id="32656-199">Grouping</span></span> |
| --- | --- |
| <span data-ttu-id="32656-200">(re)</span><span class="sxs-lookup"><span data-stu-id="32656-200">(re)</span></span> | <span data-ttu-id="32656-201">編號擷取群組 (子符合)</span><span class="sxs-lookup"><span data-stu-id="32656-201">numbered capturing group (submatch)</span></span> |
| <span data-ttu-id="32656-202">(?P&lt;名稱&gt;re)</span><span class="sxs-lookup"><span data-stu-id="32656-202">(?P&lt;name&gt;re)</span></span> | <span data-ttu-id="32656-203">具名&amp;編號擷取群組 (子符合)</span><span class="sxs-lookup"><span data-stu-id="32656-203">named &amp; numbered capturing group (submatch)</span></span> |
| <span data-ttu-id="32656-204">(?&lt;名稱&gt;re)</span><span class="sxs-lookup"><span data-stu-id="32656-204">(?&lt;name&gt;re)</span></span> | <span data-ttu-id="32656-205">具名 &amp; 編號擷取群組 (子符合) (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-205">named &amp; numbered capturing group (submatch) (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-206">(?&#39;name&#39;re)</span><span class="sxs-lookup"><span data-stu-id="32656-206">(?&#39;name&#39;re)</span></span> | <span data-ttu-id="32656-207">具名 &amp; 編號擷取群組 (子符合) (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-207">named &amp; numbered capturing group (submatch) (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-208">(?:re)</span><span class="sxs-lookup"><span data-stu-id="32656-208">(?:re)</span></span> | <span data-ttu-id="32656-209">非擷取群組</span><span class="sxs-lookup"><span data-stu-id="32656-209">non-capturing group</span></span> |
| <span data-ttu-id="32656-210">(?flags)</span><span class="sxs-lookup"><span data-stu-id="32656-210">(?flags)</span></span> | <span data-ttu-id="32656-211">在目前的群組內設定旗標；非擷取</span><span class="sxs-lookup"><span data-stu-id="32656-211">set flags within current group; non-capturing</span></span> |
| <span data-ttu-id="32656-212">(?flags:re)</span><span class="sxs-lookup"><span data-stu-id="32656-212">(?flags:re)</span></span> | <span data-ttu-id="32656-213">在 re 期間設定旗標；非擷取</span><span class="sxs-lookup"><span data-stu-id="32656-213">set flags during re; non-capturing</span></span> |
| <span data-ttu-id="32656-214">(?#text)</span><span class="sxs-lookup"><span data-stu-id="32656-214">(?#text)</span></span> | <span data-ttu-id="32656-215">注釋 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-215">comment (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-216">(?\|x\|y\|z)</span><span class="sxs-lookup"><span data-stu-id="32656-216">(?\|x\|y\|z)</span></span> | <span data-ttu-id="32656-217">分支編號重設 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-217">branch numbering reset (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-218">(?&gt;re)</span><span class="sxs-lookup"><span data-stu-id="32656-218">(?&gt;re)</span></span> | <span data-ttu-id="32656-219">re 的所有格匹配 (不支持)</span><span class="sxs-lookup"><span data-stu-id="32656-219">possessive match of re (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-220">re@&gt;</span><span class="sxs-lookup"><span data-stu-id="32656-220">re@&gt;</span></span> | <span data-ttu-id="32656-221">re 的所有格匹配 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-221">possessive match of re (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-222">%(re)</span><span class="sxs-lookup"><span data-stu-id="32656-222">%(re)</span></span> | <span data-ttu-id="32656-223">非擷取群組 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-223">non-capturing group (NOT SUPPORTED) VIM</span></span> |

|&nbsp;| <span data-ttu-id="32656-224">Flags</span><span class="sxs-lookup"><span data-stu-id="32656-224">Flags</span></span> |
| --- | --- |
| <span data-ttu-id="32656-225">i</span><span class="sxs-lookup"><span data-stu-id="32656-225">i</span></span> | <span data-ttu-id="32656-226">不區分大小寫 (預設為 false)</span><span class="sxs-lookup"><span data-stu-id="32656-226">case-insensitive (default false)</span></span> |
| <span data-ttu-id="32656-227">m</span><span class="sxs-lookup"><span data-stu-id="32656-227">m</span></span> | <span data-ttu-id="32656-228">多行模式：除了開始/結束文字 (預設為 false) 以外，還能有 ^ 和 $ 符合開始/結束行。</span><span class="sxs-lookup"><span data-stu-id="32656-228">multi-line mode: ^ and $ match begin/end line in addition to begin/end text (default false)</span></span> |
| <span data-ttu-id="32656-229">s</span><span class="sxs-lookup"><span data-stu-id="32656-229">s</span></span> | <span data-ttu-id="32656-230">let .</span><span class="sxs-lookup"><span data-stu-id="32656-230">let .</span></span> <span data-ttu-id="32656-231">符合 \n (預設為 false)</span><span class="sxs-lookup"><span data-stu-id="32656-231">match \n (default false)</span></span> |
| <span data-ttu-id="32656-232">U</span><span class="sxs-lookup"><span data-stu-id="32656-232">U</span></span> | <span data-ttu-id="32656-233">ungreedy：交換 x\* 和 x\*?、x+ 和 x+? 等的意義 (預設為 false)</span><span class="sxs-lookup"><span data-stu-id="32656-233">ungreedy: swap meaning of x\* and x\*?, x+ and x+?, etc (default false)</span></span> |

<span data-ttu-id="32656-234">旗標語法為 xyz (set) 或 -xyz (clear) 或 xy-z (設定為 xy、clear z)。</span><span class="sxs-lookup"><span data-stu-id="32656-234">Flag syntax is xyz (set) or -xyz (clear) or xy-z (set xy, clear z).</span></span>

|&nbsp;| <span data-ttu-id="32656-235">空字串</span><span class="sxs-lookup"><span data-stu-id="32656-235">Empty strings</span></span> |
| --- | --- |
| ^ | <span data-ttu-id="32656-236">文字或行的開頭 (m=true)</span><span class="sxs-lookup"><span data-stu-id="32656-236">at beginning of text or line (m=true)</span></span> |
| $ | <span data-ttu-id="32656-237">文字 (例如 \z 非 \Z) 或行的結尾 (m=true)</span><span class="sxs-lookup"><span data-stu-id="32656-237">at end of text (like \z not \Z) or line (m=true)</span></span> |
| <span data-ttu-id="32656-238">\A</span><span class="sxs-lookup"><span data-stu-id="32656-238">\A</span></span> | <span data-ttu-id="32656-239">文字的開頭</span><span class="sxs-lookup"><span data-stu-id="32656-239">at beginning of text</span></span> |
| <span data-ttu-id="32656-240">\b</span><span class="sxs-lookup"><span data-stu-id="32656-240">\b</span></span> | <span data-ttu-id="32656-241">在 ASCII 字的邊界 (一邊是\w，另一邊是 \W, \A, or \z)</span><span class="sxs-lookup"><span data-stu-id="32656-241">at ASCII word boundary (\w on one side and \W, \A, or \z on the other)</span></span> |
| <span data-ttu-id="32656-242">\B</span><span class="sxs-lookup"><span data-stu-id="32656-242">\B</span></span> | <span data-ttu-id="32656-243">不在 ASCII 字的邊界</span><span class="sxs-lookup"><span data-stu-id="32656-243">not at ASCII word boundary</span></span> |
| <span data-ttu-id="32656-244">\g</span><span class="sxs-lookup"><span data-stu-id="32656-244">\g</span></span> | <span data-ttu-id="32656-245">搜尋的次文字的開頭處 (不支援) PCRE</span><span class="sxs-lookup"><span data-stu-id="32656-245">at beginning of subtext being searched (NOT SUPPORTED) PCRE</span></span> |
| <span data-ttu-id="32656-246">\G</span><span class="sxs-lookup"><span data-stu-id="32656-246">\G</span></span> | <span data-ttu-id="32656-247">最近符合的結尾處 (不支援) PERL</span><span class="sxs-lookup"><span data-stu-id="32656-247">at end of last match (NOT SUPPORTED) PERL</span></span> |
| <span data-ttu-id="32656-248">\Z</span><span class="sxs-lookup"><span data-stu-id="32656-248">\Z</span></span> | <span data-ttu-id="32656-249">在文字結尾處，或文字結尾處的新行字元之前 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-249">at end of text, or before newline at end of text (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-250">\z</span><span class="sxs-lookup"><span data-stu-id="32656-250">\z</span></span> | <span data-ttu-id="32656-251">在文字結尾處</span><span class="sxs-lookup"><span data-stu-id="32656-251">at end of text</span></span> |
| <span data-ttu-id="32656-252">(?=re)</span><span class="sxs-lookup"><span data-stu-id="32656-252">(?=re)</span></span> | <span data-ttu-id="32656-253">在文字與 re 相符之前 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-253">before text matching re (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-254">(?!re)</span><span class="sxs-lookup"><span data-stu-id="32656-254">(?!re)</span></span> | <span data-ttu-id="32656-255">在文字不符合 re 之前 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-255">before text not matching re (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-256">(?&lt;=re)</span><span class="sxs-lookup"><span data-stu-id="32656-256">(?&lt;=re)</span></span> | <span data-ttu-id="32656-257">在文字與 re 相符之后 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-257">after text matching re (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-258">(?&lt;!re)</span><span class="sxs-lookup"><span data-stu-id="32656-258">(?&lt;!re)</span></span> | <span data-ttu-id="32656-259">在文字與 re 不相符之后 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-259">after text not matching re (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-260">re&amp;</span><span class="sxs-lookup"><span data-stu-id="32656-260">re&amp;</span></span> | <span data-ttu-id="32656-261">在文字與 re 相符之前 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-261">before text matching re (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-262">re@=</span><span class="sxs-lookup"><span data-stu-id="32656-262">re@=</span></span> | <span data-ttu-id="32656-263">在文字與 re 相符之前 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-263">before text matching re (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-264">re@!</span><span class="sxs-lookup"><span data-stu-id="32656-264">re@!</span></span> | <span data-ttu-id="32656-265">在文字不符合 re 之前 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-265">before text not matching re (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-266">re@&lt;=</span><span class="sxs-lookup"><span data-stu-id="32656-266">re@&lt;=</span></span> | <span data-ttu-id="32656-267">在文字與 re 相符之后 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-267">after text matching re (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-268">re@&lt;!</span><span class="sxs-lookup"><span data-stu-id="32656-268">re@&lt;!</span></span> | <span data-ttu-id="32656-269">在文字與 re 不相符之后 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-269">after text not matching re (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-270">\zs</span><span class="sxs-lookup"><span data-stu-id="32656-270">\zs</span></span> | <span data-ttu-id="32656-271">開始匹配組 (= \K) (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-271">sets start of match (= \K) (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-272">\ze</span><span class="sxs-lookup"><span data-stu-id="32656-272">\ze</span></span> | <span data-ttu-id="32656-273">結束匹配組 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-273">sets end of match (NOT SUPPORTED) VIM</span></span> |
| \%^ | <span data-ttu-id="32656-274">檔案開頭 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-274">beginning of file (NOT SUPPORTED) VIM</span></span> |
| \%$ | <span data-ttu-id="32656-275">檔案結尾 (不支持) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-275">end of file (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-276">\%V</span><span class="sxs-lookup"><span data-stu-id="32656-276">\%V</span></span> | <span data-ttu-id="32656-277">在螢幕上 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-277">on screen (NOT SUPPORTED) VIM</span></span> |
| \%# | <span data-ttu-id="32656-278">游標位置 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-278">cursor position (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-279">\%&#39;m</span><span class="sxs-lookup"><span data-stu-id="32656-279">\%&#39;m</span></span> | <span data-ttu-id="32656-280">標記 m 位置 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-280">mark m position (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-281">\%23l</span><span class="sxs-lookup"><span data-stu-id="32656-281">\%23l</span></span> | <span data-ttu-id="32656-282">在行 23 中 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-282">in line 23 (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-283">\%23c</span><span class="sxs-lookup"><span data-stu-id="32656-283">\%23c</span></span> | <span data-ttu-id="32656-284">在欄 23 中 (不支援) VIM </span><span class="sxs-lookup"><span data-stu-id="32656-284">in column 23 (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-285">\%23v</span><span class="sxs-lookup"><span data-stu-id="32656-285">\%23v</span></span> | <span data-ttu-id="32656-286">在虛擬欄 23 中 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-286">in virtual column 23 (NOT SUPPORTED) VIM</span></span> |

|&nbsp;| <span data-ttu-id="32656-287">逸出序列</span><span class="sxs-lookup"><span data-stu-id="32656-287">Escape sequences</span></span> |
| --- | --- |
| <span data-ttu-id="32656-288">\a</span><span class="sxs-lookup"><span data-stu-id="32656-288">\a</span></span> | <span data-ttu-id="32656-289">bell (≡ \007)</span><span class="sxs-lookup"><span data-stu-id="32656-289">bell (≡ \007)</span></span> |
| <span data-ttu-id="32656-290">\f</span><span class="sxs-lookup"><span data-stu-id="32656-290">\f</span></span> | <span data-ttu-id="32656-291">表單摘要 (≡ \014)</span><span class="sxs-lookup"><span data-stu-id="32656-291">form feed (≡ \014)</span></span> |
| <span data-ttu-id="32656-292">\t</span><span class="sxs-lookup"><span data-stu-id="32656-292">\t</span></span> | <span data-ttu-id="32656-293">水平索引標籤 (≡ \011)</span><span class="sxs-lookup"><span data-stu-id="32656-293">horizontal tab (≡ \011)</span></span> |
| <span data-ttu-id="32656-294">\n</span><span class="sxs-lookup"><span data-stu-id="32656-294">\n</span></span> | <span data-ttu-id="32656-295">新行字元 (≡ \012)</span><span class="sxs-lookup"><span data-stu-id="32656-295">newline (≡ \012)</span></span> |
| <span data-ttu-id="32656-296">\r</span><span class="sxs-lookup"><span data-stu-id="32656-296">\r</span></span> | <span data-ttu-id="32656-297">滑動架傳回 (≡ \015)</span><span class="sxs-lookup"><span data-stu-id="32656-297">carriage return (≡ \015)</span></span> |
| <span data-ttu-id="32656-298">\v</span><span class="sxs-lookup"><span data-stu-id="32656-298">\v</span></span> | <span data-ttu-id="32656-299">垂直定位字元 (≡ \013)</span><span class="sxs-lookup"><span data-stu-id="32656-299">vertical tab character (≡ \013)</span></span> |
| \* | <span data-ttu-id="32656-300">常值 \*，適用于任何標點字元 \*</span><span class="sxs-lookup"><span data-stu-id="32656-300">literal \*, for any punctuation character \*</span></span> |
| <span data-ttu-id="32656-301">\123</span><span class="sxs-lookup"><span data-stu-id="32656-301">\123</span></span> | <span data-ttu-id="32656-302">八進位字元代碼 (最多三個數字)</span><span class="sxs-lookup"><span data-stu-id="32656-302">octal character code (up to three digits)</span></span> |
| <span data-ttu-id="32656-303">\x7F</span><span class="sxs-lookup"><span data-stu-id="32656-303">\x7F</span></span> | <span data-ttu-id="32656-304">十六進位字元碼 (正好兩個數字)</span><span class="sxs-lookup"><span data-stu-id="32656-304">hex character code (exactly two digits)</span></span> |
| <span data-ttu-id="32656-305">\x{10FFFF}</span><span class="sxs-lookup"><span data-stu-id="32656-305">\x{10FFFF}</span></span> | <span data-ttu-id="32656-306">十六進位字元代碼</span><span class="sxs-lookup"><span data-stu-id="32656-306">hex character code</span></span> |
| <span data-ttu-id="32656-307">\C</span><span class="sxs-lookup"><span data-stu-id="32656-307">\C</span></span> | <span data-ttu-id="32656-308">即使在 UTF-8 模式中也與單一位元組相符</span><span class="sxs-lookup"><span data-stu-id="32656-308">match a single byte even in UTF-8 mode</span></span> |
| <span data-ttu-id="32656-309">\Q...\E</span><span class="sxs-lookup"><span data-stu-id="32656-309">\Q...\E</span></span> | <span data-ttu-id="32656-310">常值文字 ... 即使 ... 有標點符號</span><span class="sxs-lookup"><span data-stu-id="32656-310">literal text ... even if ... has punctuation</span></span> |
| <span data-ttu-id="32656-311">\1</span><span class="sxs-lookup"><span data-stu-id="32656-311">\1</span></span> | <span data-ttu-id="32656-312">反向參考 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-312">backreference (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-313">\b</span><span class="sxs-lookup"><span data-stu-id="32656-313">\b</span></span> | <span data-ttu-id="32656-314">退格鍵 (不支援) (使用 \ 010)</span><span class="sxs-lookup"><span data-stu-id="32656-314">backspace (NOT SUPPORTED) (use \010)</span></span> |
| <span data-ttu-id="32656-315">\cK</span><span class="sxs-lookup"><span data-stu-id="32656-315">\cK</span></span> | <span data-ttu-id="32656-316">控制 char ^K (不支援) (使用 \001 等)</span><span class="sxs-lookup"><span data-stu-id="32656-316">control char ^K (NOT SUPPORTED) (use \001 etc)</span></span> |
| <span data-ttu-id="32656-317">\e</span><span class="sxs-lookup"><span data-stu-id="32656-317">\e</span></span> | <span data-ttu-id="32656-318">逸出 (不支援) (使用 \033)</span><span class="sxs-lookup"><span data-stu-id="32656-318">escape (NOT SUPPORTED) (use \033)</span></span> |
| <span data-ttu-id="32656-319">\g1</span><span class="sxs-lookup"><span data-stu-id="32656-319">\g1</span></span> | <span data-ttu-id="32656-320">反向參考 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-320">backreference (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-321">\g{1}</span><span class="sxs-lookup"><span data-stu-id="32656-321">\g{1}</span></span> | <span data-ttu-id="32656-322">反向參考 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-322">backreference (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-323">\g{+1}</span><span class="sxs-lookup"><span data-stu-id="32656-323">\g{+1}</span></span> | <span data-ttu-id="32656-324">反向參考 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-324">backreference (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-325">\g{-1}</span><span class="sxs-lookup"><span data-stu-id="32656-325">\g{-1}</span></span> | <span data-ttu-id="32656-326">反向參考 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-326">backreference (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-327">\g{name}</span><span class="sxs-lookup"><span data-stu-id="32656-327">\g{name}</span></span> | <span data-ttu-id="32656-328">具名反向參考 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-328">named backreference (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-329">\g&lt;名稱&gt;</span><span class="sxs-lookup"><span data-stu-id="32656-329">\g&lt;name&gt;</span></span> | <span data-ttu-id="32656-330">副程式撥號 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-330">subroutine call (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-331">\g&#39;name&#39;</span><span class="sxs-lookup"><span data-stu-id="32656-331">\g&#39;name&#39;</span></span> | <span data-ttu-id="32656-332">副程式撥號 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-332">subroutine call (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-333">\k&lt;名稱&gt;</span><span class="sxs-lookup"><span data-stu-id="32656-333">\k&lt;name&gt;</span></span> | <span data-ttu-id="32656-334">具名反向參考 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-334">named backreference (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-335">\k&#39;name&#39;</span><span class="sxs-lookup"><span data-stu-id="32656-335">\k&#39;name&#39;</span></span> | <span data-ttu-id="32656-336">具名反向參考 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-336">named backreference (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-337">\lX</span><span class="sxs-lookup"><span data-stu-id="32656-337">\lX</span></span> | <span data-ttu-id="32656-338">小寫 X (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-338">lowercase X (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-339">\ux</span><span class="sxs-lookup"><span data-stu-id="32656-339">\ux</span></span> | <span data-ttu-id="32656-340">大寫 x (不支持)</span><span class="sxs-lookup"><span data-stu-id="32656-340">uppercase x (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-341">\L...\E</span><span class="sxs-lookup"><span data-stu-id="32656-341">\L...\E</span></span> | <span data-ttu-id="32656-342">小寫文字 ... (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-342">lowercase text ... (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-343">\K</span><span class="sxs-lookup"><span data-stu-id="32656-343">\K</span></span> | <span data-ttu-id="32656-344">重設 $0 的開頭 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-344">reset beginning of $0 (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-345">\N{name}</span><span class="sxs-lookup"><span data-stu-id="32656-345">\N{name}</span></span> | <span data-ttu-id="32656-346">具名 Unicode 字元 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-346">named Unicode character (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-347">\R</span><span class="sxs-lookup"><span data-stu-id="32656-347">\R</span></span> | <span data-ttu-id="32656-348">分行符號 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-348">line break (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-349">\U...\E</span><span class="sxs-lookup"><span data-stu-id="32656-349">\U...\E</span></span> | <span data-ttu-id="32656-350">大寫文字 ... (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-350">upper case text ... (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-351">\X</span><span class="sxs-lookup"><span data-stu-id="32656-351">\X</span></span> | <span data-ttu-id="32656-352">擴充 Unicode 序列 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-352">extended Unicode sequence (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-353">\%d123</span><span class="sxs-lookup"><span data-stu-id="32656-353">\%d123</span></span> | <span data-ttu-id="32656-354">十進位字元 123 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-354">decimal character 123 (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-355">\%xFF</span><span class="sxs-lookup"><span data-stu-id="32656-355">\%xFF</span></span> | <span data-ttu-id="32656-356">十六進位字元 FF (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-356">hex character FF (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-357">\%o123</span><span class="sxs-lookup"><span data-stu-id="32656-357">\%o123</span></span> | <span data-ttu-id="32656-358">八進位字元 123 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-358">octal character 123 (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-359">\%u1234</span><span class="sxs-lookup"><span data-stu-id="32656-359">\%u1234</span></span> | <span data-ttu-id="32656-360">Unicode 字元 0x1234 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-360">Unicode character 0x1234 (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-361">\%U12345678</span><span class="sxs-lookup"><span data-stu-id="32656-361">\%U12345678</span></span> | <span data-ttu-id="32656-362">Unicode 字元 0x12345678 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-362">Unicode character 0x12345678 (NOT SUPPORTED) VIM</span></span> |

|&nbsp;| <span data-ttu-id="32656-363">字元類別元素</span><span class="sxs-lookup"><span data-stu-id="32656-363">Character class elements</span></span> |
| --- | --- |
| <span data-ttu-id="32656-364">x</span><span class="sxs-lookup"><span data-stu-id="32656-364">x</span></span> | <span data-ttu-id="32656-365">單一字元</span><span class="sxs-lookup"><span data-stu-id="32656-365">single character</span></span> |
| <span data-ttu-id="32656-366">A-Z</span><span class="sxs-lookup"><span data-stu-id="32656-366">A-Z</span></span> | <span data-ttu-id="32656-367">字元範圍 (全人)</span><span class="sxs-lookup"><span data-stu-id="32656-367">character range (inclusive)</span></span> |
| <span data-ttu-id="32656-368">\d</span><span class="sxs-lookup"><span data-stu-id="32656-368">\d</span></span> | <span data-ttu-id="32656-369">Perl 字元類別</span><span class="sxs-lookup"><span data-stu-id="32656-369">Perl character class</span></span> |
| <span data-ttu-id="32656-370">[:foo:]</span><span class="sxs-lookup"><span data-stu-id="32656-370">[:foo:]</span></span> | <span data-ttu-id="32656-371">ASCII 字元類別 foo</span><span class="sxs-lookup"><span data-stu-id="32656-371">ASCII character class foo</span></span> |
| <span data-ttu-id="32656-372">\p{Foo}</span><span class="sxs-lookup"><span data-stu-id="32656-372">\p{Foo}</span></span> | <span data-ttu-id="32656-373">Unicode 字元類別 Foo</span><span class="sxs-lookup"><span data-stu-id="32656-373">Unicode character class Foo</span></span> |
| <span data-ttu-id="32656-374">\pF</span><span class="sxs-lookup"><span data-stu-id="32656-374">\pF</span></span> | <span data-ttu-id="32656-375">Unicode 字元類別 F (單字母名稱)</span><span class="sxs-lookup"><span data-stu-id="32656-375">Unicode character class F (one-letter name)</span></span> |

|&nbsp;| <span data-ttu-id="32656-376">具名字元類作為字元類元素</span><span class="sxs-lookup"><span data-stu-id="32656-376">Named character classes as character class elements</span></span> |
| --- | --- |
| <span data-ttu-id="32656-377">[\d]</span><span class="sxs-lookup"><span data-stu-id="32656-377">[\d]</span></span> | <span data-ttu-id="32656-378">數位 (≡ \d)</span><span class="sxs-lookup"><span data-stu-id="32656-378">digits (≡ \d)</span></span> |
| <span data-ttu-id="32656-379">[^\d]</span><span class="sxs-lookup"><span data-stu-id="32656-379">[^\d]</span></span> | <span data-ttu-id="32656-380">非數位 (≡ \D)</span><span class="sxs-lookup"><span data-stu-id="32656-380">not digits (≡ \D)</span></span> |
| <span data-ttu-id="32656-381">[\D]</span><span class="sxs-lookup"><span data-stu-id="32656-381">[\D]</span></span> | <span data-ttu-id="32656-382">非數位 (≡ \D)</span><span class="sxs-lookup"><span data-stu-id="32656-382">not digits (≡ \D)</span></span> |
| <span data-ttu-id="32656-383">[^\D]</span><span class="sxs-lookup"><span data-stu-id="32656-383">[^\D]</span></span> | <span data-ttu-id="32656-384">否非數位 (≡ \d)</span><span class="sxs-lookup"><span data-stu-id="32656-384">not not digits (≡ \d)</span></span> |
| <span data-ttu-id="32656-385">[[:name:]]</span><span class="sxs-lookup"><span data-stu-id="32656-385">[[:name:]]</span></span> | <span data-ttu-id="32656-386">字元類別中的具名 ASCII 類別 (≡ [:name:])</span><span class="sxs-lookup"><span data-stu-id="32656-386">named ASCII class inside character class (≡ [:name:])</span></span> |
| <span data-ttu-id="32656-387">[^[:name:]]</span><span class="sxs-lookup"><span data-stu-id="32656-387">[^[:name:]]</span></span> | <span data-ttu-id="32656-388">在反字元類中的具名 ASCII 類別 (≡ [:^name:])</span><span class="sxs-lookup"><span data-stu-id="32656-388">named ASCII class inside negated character class (≡ [:^name:])</span></span> |
| <span data-ttu-id="32656-389">[\p{Name}]</span><span class="sxs-lookup"><span data-stu-id="32656-389">[\p{Name}]</span></span> | <span data-ttu-id="32656-390">字元類別中的具名 Unicode 屬性 (≡ \p{Name})</span><span class="sxs-lookup"><span data-stu-id="32656-390">named Unicode property inside character class (≡ \p{Name})</span></span> |
| <span data-ttu-id="32656-391">[^\p{Name}]</span><span class="sxs-lookup"><span data-stu-id="32656-391">[^\p{Name}]</span></span> | <span data-ttu-id="32656-392">反字元類別中的具名 Unicode 屬性 (≡ \p{Name})</span><span class="sxs-lookup"><span data-stu-id="32656-392">named Unicode property inside negated character class (≡ \P{Name})</span></span> |

| <a name="user-content-perl"></a> | <span data-ttu-id="32656-393">Perl 字元類 (全為 ASCII)</span><span class="sxs-lookup"><span data-stu-id="32656-393">Perl character classes (all ASCII-only)</span></span> |
| --- | --- |
| <span data-ttu-id="32656-394">\d</span><span class="sxs-lookup"><span data-stu-id="32656-394">\d</span></span> | <span data-ttu-id="32656-395">位數 (≡ [0-9])</span><span class="sxs-lookup"><span data-stu-id="32656-395">digits (≡ [0-9])</span></span> |
| <span data-ttu-id="32656-396">\D</span><span class="sxs-lookup"><span data-stu-id="32656-396">\D</span></span> | <span data-ttu-id="32656-397">非位數 (≡ [^0-9])</span><span class="sxs-lookup"><span data-stu-id="32656-397">not digits (≡ [^0-9])</span></span> |
| <span data-ttu-id="32656-398">\s</span><span class="sxs-lookup"><span data-stu-id="32656-398">\s</span></span> | <span data-ttu-id="32656-399">空格 (≡ [\t\n\f\r])</span><span class="sxs-lookup"><span data-stu-id="32656-399">whitespace (≡ [\t\n\f\r])</span></span> |
| <span data-ttu-id="32656-400">\S</span><span class="sxs-lookup"><span data-stu-id="32656-400">\S</span></span> | <span data-ttu-id="32656-401">非空格 (≡ [^\t\n\f\r])</span><span class="sxs-lookup"><span data-stu-id="32656-401">not whitespace (≡ [^\t\n\f\r])</span></span> |
| <span data-ttu-id="32656-402">\w</span><span class="sxs-lookup"><span data-stu-id="32656-402">\w</span></span> | <span data-ttu-id="32656-403">文字字元 (≡ [0-9A-Za-z\_])</span><span class="sxs-lookup"><span data-stu-id="32656-403">word characters (≡ [0-9A-Za-z\_])</span></span> |
| <span data-ttu-id="32656-404">\W</span><span class="sxs-lookup"><span data-stu-id="32656-404">\W</span></span> | <span data-ttu-id="32656-405">非文字字元 (≡ [^0-9A-Za-z\_])</span><span class="sxs-lookup"><span data-stu-id="32656-405">not word characters (≡ [^0-9A-Za-z\_])</span></span> |
| <span data-ttu-id="32656-406">\h</span><span class="sxs-lookup"><span data-stu-id="32656-406">\h</span></span> | <span data-ttu-id="32656-407">水平空間 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-407">horizontal space (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-408">\H</span><span class="sxs-lookup"><span data-stu-id="32656-408">\H</span></span> | <span data-ttu-id="32656-409">非水平空間 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-409">not horizontal space (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-410">\v</span><span class="sxs-lookup"><span data-stu-id="32656-410">\v</span></span> | <span data-ttu-id="32656-411">垂直空間 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-411">vertical space (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-412">\V</span><span class="sxs-lookup"><span data-stu-id="32656-412">\V</span></span> | <span data-ttu-id="32656-413">非垂直空間 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-413">not vertical space (NOT SUPPORTED)</span></span> |

|<a name="user-content-ascii"></a>  | <span data-ttu-id="32656-414">ASCII 字元類別</span><span class="sxs-lookup"><span data-stu-id="32656-414">ASCII character classes</span></span> |
| --- | --- |
| <span data-ttu-id="32656-415">[[:alnum:]]</span><span class="sxs-lookup"><span data-stu-id="32656-415">[[:alnum:]]</span></span> | <span data-ttu-id="32656-416">英數字元 (≡ [0-9A-Za-z])</span><span class="sxs-lookup"><span data-stu-id="32656-416">alphanumeric (≡ [0-9A-Za-z])</span></span> |
| <span data-ttu-id="32656-417">[[:alpha:]]</span><span class="sxs-lookup"><span data-stu-id="32656-417">[[:alpha:]]</span></span> | <span data-ttu-id="32656-418">字母 (≡ [A-Za-z])</span><span class="sxs-lookup"><span data-stu-id="32656-418">alphabetic (≡ [A-Za-z])</span></span> |
| <span data-ttu-id="32656-419">[[:ascii:]]</span><span class="sxs-lookup"><span data-stu-id="32656-419">[[:ascii:]]</span></span> | <span data-ttu-id="32656-420">ASCII (≡ [\x00-\x7F])</span><span class="sxs-lookup"><span data-stu-id="32656-420">ASCII (≡ [\x00-\x7F])</span></span> |
| <span data-ttu-id="32656-421">[[:blank:]]</span><span class="sxs-lookup"><span data-stu-id="32656-421">[[:blank:]]</span></span> | <span data-ttu-id="32656-422">空白(≡ [\t])</span><span class="sxs-lookup"><span data-stu-id="32656-422">blank (≡ [\t])</span></span> |
| <span data-ttu-id="32656-423">[[:cntrl:]]</span><span class="sxs-lookup"><span data-stu-id="32656-423">[[:cntrl:]]</span></span> | <span data-ttu-id="32656-424">控制項 (≡ [\x00-\x1F\x7F])</span><span class="sxs-lookup"><span data-stu-id="32656-424">control (≡ [\x00-\x1F\x7F])</span></span> |
| <span data-ttu-id="32656-425">[[:d igit：]]</span><span class="sxs-lookup"><span data-stu-id="32656-425">[[:digit:]]</span></span> | <span data-ttu-id="32656-426">位數 (≡ [0-9])</span><span class="sxs-lookup"><span data-stu-id="32656-426">digits (≡ [0-9])</span></span> |
| <span data-ttu-id="32656-427">[[:graph:]]</span><span class="sxs-lookup"><span data-stu-id="32656-427">[[:graph:]]</span></span> | <span data-ttu-id="32656-428">圖形化 (≡ `[!-~]` ≡ `[A-Za-z0-9!&quot;#$%&amp;&#39;()\*+,\-./:;&lt;=&gt;?@[\\\]^_`\` `{\|}~]`)</span><span class="sxs-lookup"><span data-stu-id="32656-428">graphical (≡ `[!-~]` ≡ `[A-Za-z0-9!&quot;#$%&amp;&#39;()\*+,\-./:;&lt;=&gt;?@[\\\]^_`\` `{\|}~]`)</span></span> |
| <span data-ttu-id="32656-429">[[:lower:]]</span><span class="sxs-lookup"><span data-stu-id="32656-429">[[:lower:]]</span></span> | <span data-ttu-id="32656-430">小寫 (≡ [a-z])</span><span class="sxs-lookup"><span data-stu-id="32656-430">lower case (≡ [a-z])</span></span> |
| <span data-ttu-id="32656-431">[[:print:]]</span><span class="sxs-lookup"><span data-stu-id="32656-431">[[:print:]]</span></span> | <span data-ttu-id="32656-432">可列印 (≡ [-~] ≡ [[:graph:]])</span><span class="sxs-lookup"><span data-stu-id="32656-432">printable (≡ [-~] ≡ [[:graph:]])</span></span> |
| <span data-ttu-id="32656-433">[[:punct:]]</span><span class="sxs-lookup"><span data-stu-id="32656-433">[[:punct:]]</span></span> | <span data-ttu-id="32656-434">標點符號 (≡ [!-/:-@[-\`{-~])</span><span class="sxs-lookup"><span data-stu-id="32656-434">punctuation (≡ [!-/:-@[-\`{-~])</span></span> |
| <span data-ttu-id="32656-435">[[:space:]]</span><span class="sxs-lookup"><span data-stu-id="32656-435">[[:space:]]</span></span> | <span data-ttu-id="32656-436">空格 (≡ [\t\n\v\f\r])</span><span class="sxs-lookup"><span data-stu-id="32656-436">whitespace (≡ [\t\n\v\f\r])</span></span> |
| <span data-ttu-id="32656-437">[[:upper:]]</span><span class="sxs-lookup"><span data-stu-id="32656-437">[[:upper:]]</span></span> | <span data-ttu-id="32656-438">大寫 (≡ [A-Z])</span><span class="sxs-lookup"><span data-stu-id="32656-438">upper case (≡ [A-Z])</span></span> |
| <span data-ttu-id="32656-439">[[:word:]]</span><span class="sxs-lookup"><span data-stu-id="32656-439">[[:word:]]</span></span> | <span data-ttu-id="32656-440">文字字元 (≡ [0-9A-Za-z\_])</span><span class="sxs-lookup"><span data-stu-id="32656-440">word characters (≡ [0-9A-Za-z\_])</span></span> |
| <span data-ttu-id="32656-441">[[:xdigit:]]</span><span class="sxs-lookup"><span data-stu-id="32656-441">[[:xdigit:]]</span></span> | <span data-ttu-id="32656-442">十六進位數位 (≡ [0-9A-Fa-f])</span><span class="sxs-lookup"><span data-stu-id="32656-442">hex digit (≡ [0-9A-Fa-f])</span></span> |

|&nbsp;| <span data-ttu-id="32656-443">Unicode 字元類名 --一般類別</span><span class="sxs-lookup"><span data-stu-id="32656-443">Unicode character class names--general category</span></span> |
| --- | --- |
| <span data-ttu-id="32656-444">C</span><span class="sxs-lookup"><span data-stu-id="32656-444">C</span></span> | <span data-ttu-id="32656-445">其他</span><span class="sxs-lookup"><span data-stu-id="32656-445">other</span></span> |
| <span data-ttu-id="32656-446">副本</span><span class="sxs-lookup"><span data-stu-id="32656-446">Cc</span></span> | <span data-ttu-id="32656-447">control</span><span class="sxs-lookup"><span data-stu-id="32656-447">control</span></span> |
| <span data-ttu-id="32656-448">Cf</span><span class="sxs-lookup"><span data-stu-id="32656-448">Cf</span></span> | <span data-ttu-id="32656-449">format</span><span class="sxs-lookup"><span data-stu-id="32656-449">format</span></span> |
| <span data-ttu-id="32656-450">Cn</span><span class="sxs-lookup"><span data-stu-id="32656-450">Cn</span></span> | <span data-ttu-id="32656-451">未指派的代碼點 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-451">unassigned code points (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-452">Co</span><span class="sxs-lookup"><span data-stu-id="32656-452">Co</span></span> | <span data-ttu-id="32656-453">私密用法</span><span class="sxs-lookup"><span data-stu-id="32656-453">private use</span></span> |
| <span data-ttu-id="32656-454">Cs</span><span class="sxs-lookup"><span data-stu-id="32656-454">Cs</span></span> | <span data-ttu-id="32656-455">替代</span><span class="sxs-lookup"><span data-stu-id="32656-455">surrogate</span></span> |
| <span data-ttu-id="32656-456">L</span><span class="sxs-lookup"><span data-stu-id="32656-456">L</span></span> | <span data-ttu-id="32656-457">字母</span><span class="sxs-lookup"><span data-stu-id="32656-457">letter</span></span> |
| <span data-ttu-id="32656-458">LC</span><span class="sxs-lookup"><span data-stu-id="32656-458">LC</span></span> | <span data-ttu-id="32656-459">大小寫字母 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-459">cased letter (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-460">L&amp;</span><span class="sxs-lookup"><span data-stu-id="32656-460">L&amp;</span></span> | <span data-ttu-id="32656-461">大小寫字母 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-461">cased letter (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-462">Ll</span><span class="sxs-lookup"><span data-stu-id="32656-462">Ll</span></span> | <span data-ttu-id="32656-463">小寫字母</span><span class="sxs-lookup"><span data-stu-id="32656-463">lowercase letter</span></span> |
| <span data-ttu-id="32656-464">Lm</span><span class="sxs-lookup"><span data-stu-id="32656-464">Lm</span></span> | <span data-ttu-id="32656-465">修飾詞字母</span><span class="sxs-lookup"><span data-stu-id="32656-465">modifier letter</span></span> |
| <span data-ttu-id="32656-466">Lo</span><span class="sxs-lookup"><span data-stu-id="32656-466">Lo</span></span> | <span data-ttu-id="32656-467">其他字母</span><span class="sxs-lookup"><span data-stu-id="32656-467">other letter</span></span> |
| <span data-ttu-id="32656-468">Lt</span><span class="sxs-lookup"><span data-stu-id="32656-468">Lt</span></span> | <span data-ttu-id="32656-469">大寫字母</span><span class="sxs-lookup"><span data-stu-id="32656-469">titlecase letter</span></span> |
| <span data-ttu-id="32656-470">Lu</span><span class="sxs-lookup"><span data-stu-id="32656-470">Lu</span></span> | <span data-ttu-id="32656-471">大寫字母</span><span class="sxs-lookup"><span data-stu-id="32656-471">uppercase letter</span></span> |
| <span data-ttu-id="32656-472">M</span><span class="sxs-lookup"><span data-stu-id="32656-472">M</span></span> | <span data-ttu-id="32656-473">標記</span><span class="sxs-lookup"><span data-stu-id="32656-473">mark</span></span> |
| <span data-ttu-id="32656-474">Mc</span><span class="sxs-lookup"><span data-stu-id="32656-474">Mc</span></span> | <span data-ttu-id="32656-475">間距標記</span><span class="sxs-lookup"><span data-stu-id="32656-475">spacing mark</span></span> |
| <span data-ttu-id="32656-476">Me</span><span class="sxs-lookup"><span data-stu-id="32656-476">Me</span></span> | <span data-ttu-id="32656-477">封閉標記</span><span class="sxs-lookup"><span data-stu-id="32656-477">enclosing mark</span></span> |
| <span data-ttu-id="32656-478">Mn</span><span class="sxs-lookup"><span data-stu-id="32656-478">Mn</span></span> | <span data-ttu-id="32656-479">非間距標記</span><span class="sxs-lookup"><span data-stu-id="32656-479">non-spacing mark</span></span> |
| <span data-ttu-id="32656-480">N</span><span class="sxs-lookup"><span data-stu-id="32656-480">N</span></span> | <span data-ttu-id="32656-481">數字</span><span class="sxs-lookup"><span data-stu-id="32656-481">number</span></span> |
| <span data-ttu-id="32656-482">Nd</span><span class="sxs-lookup"><span data-stu-id="32656-482">Nd</span></span> | <span data-ttu-id="32656-483">十進位數</span><span class="sxs-lookup"><span data-stu-id="32656-483">decimal number</span></span> |
| <span data-ttu-id="32656-484">Nl</span><span class="sxs-lookup"><span data-stu-id="32656-484">Nl</span></span> | <span data-ttu-id="32656-485">字母數字</span><span class="sxs-lookup"><span data-stu-id="32656-485">letter number</span></span> |
| <span data-ttu-id="32656-486">否</span><span class="sxs-lookup"><span data-stu-id="32656-486">No</span></span> | <span data-ttu-id="32656-487">其他數字</span><span class="sxs-lookup"><span data-stu-id="32656-487">other number</span></span> |
| <span data-ttu-id="32656-488">P</span><span class="sxs-lookup"><span data-stu-id="32656-488">P</span></span> | <span data-ttu-id="32656-489">標點符號</span><span class="sxs-lookup"><span data-stu-id="32656-489">punctuation</span></span> |
| <span data-ttu-id="32656-490">Pc</span><span class="sxs-lookup"><span data-stu-id="32656-490">Pc</span></span> | <span data-ttu-id="32656-491">連接器標點符號</span><span class="sxs-lookup"><span data-stu-id="32656-491">connector punctuation</span></span> |
| <span data-ttu-id="32656-492">Pd</span><span class="sxs-lookup"><span data-stu-id="32656-492">Pd</span></span> | <span data-ttu-id="32656-493">虛線標點符號</span><span class="sxs-lookup"><span data-stu-id="32656-493">dash punctuation</span></span> |
| <span data-ttu-id="32656-494">Pe</span><span class="sxs-lookup"><span data-stu-id="32656-494">Pe</span></span> | <span data-ttu-id="32656-495">關閉標點符號</span><span class="sxs-lookup"><span data-stu-id="32656-495">close punctuation</span></span> |
| <span data-ttu-id="32656-496">Pf</span><span class="sxs-lookup"><span data-stu-id="32656-496">Pf</span></span> | <span data-ttu-id="32656-497">末位標點符號</span><span class="sxs-lookup"><span data-stu-id="32656-497">final punctuation</span></span> |
| <span data-ttu-id="32656-498">Pi</span><span class="sxs-lookup"><span data-stu-id="32656-498">Pi</span></span> | <span data-ttu-id="32656-499">首位標點</span><span class="sxs-lookup"><span data-stu-id="32656-499">initial punctuation</span></span> |
| <span data-ttu-id="32656-500">Po</span><span class="sxs-lookup"><span data-stu-id="32656-500">Po</span></span> | <span data-ttu-id="32656-501">其他標點符號</span><span class="sxs-lookup"><span data-stu-id="32656-501">other punctuation</span></span> |
| <span data-ttu-id="32656-502">Ps</span><span class="sxs-lookup"><span data-stu-id="32656-502">Ps</span></span> | <span data-ttu-id="32656-503">開放標點符號</span><span class="sxs-lookup"><span data-stu-id="32656-503">open punctuation</span></span> |
| <span data-ttu-id="32656-504">S</span><span class="sxs-lookup"><span data-stu-id="32656-504">S</span></span> | <span data-ttu-id="32656-505">symbol</span><span class="sxs-lookup"><span data-stu-id="32656-505">symbol</span></span> |
| <span data-ttu-id="32656-506">Sc</span><span class="sxs-lookup"><span data-stu-id="32656-506">Sc</span></span> | <span data-ttu-id="32656-507">貨幣符號</span><span class="sxs-lookup"><span data-stu-id="32656-507">currency symbol</span></span> |
| <span data-ttu-id="32656-508">Sk</span><span class="sxs-lookup"><span data-stu-id="32656-508">Sk</span></span> | <span data-ttu-id="32656-509">修飾詞符號</span><span class="sxs-lookup"><span data-stu-id="32656-509">modifier symbol</span></span> |
| <span data-ttu-id="32656-510">Sm</span><span class="sxs-lookup"><span data-stu-id="32656-510">Sm</span></span> | <span data-ttu-id="32656-511">數學符號</span><span class="sxs-lookup"><span data-stu-id="32656-511">math symbol</span></span> |
| <span data-ttu-id="32656-512">So</span><span class="sxs-lookup"><span data-stu-id="32656-512">So</span></span> | <span data-ttu-id="32656-513">其他符號</span><span class="sxs-lookup"><span data-stu-id="32656-513">other symbol</span></span> |
| <span data-ttu-id="32656-514">Z</span><span class="sxs-lookup"><span data-stu-id="32656-514">Z</span></span> | <span data-ttu-id="32656-515">分隔符號</span><span class="sxs-lookup"><span data-stu-id="32656-515">separator</span></span> |
| <span data-ttu-id="32656-516">Zl</span><span class="sxs-lookup"><span data-stu-id="32656-516">Zl</span></span> | <span data-ttu-id="32656-517">行分隔符號</span><span class="sxs-lookup"><span data-stu-id="32656-517">line separator</span></span> |
| <span data-ttu-id="32656-518">Zp</span><span class="sxs-lookup"><span data-stu-id="32656-518">Zp</span></span> | <span data-ttu-id="32656-519">段落分隔符號</span><span class="sxs-lookup"><span data-stu-id="32656-519">paragraph separator</span></span> |
| <span data-ttu-id="32656-520">Zs</span><span class="sxs-lookup"><span data-stu-id="32656-520">Zs</span></span> | <span data-ttu-id="32656-521">空格分隔符號</span><span class="sxs-lookup"><span data-stu-id="32656-521">space separator</span></span> |

| <span data-ttu-id="32656-522">Unicode 字元類名 -- 指令碼</span><span class="sxs-lookup"><span data-stu-id="32656-522">Unicode character class names--scripts</span></span> |
| --- |
| <span data-ttu-id="32656-523">Adlam 文</span><span class="sxs-lookup"><span data-stu-id="32656-523">Adlam</span></span> |
| <span data-ttu-id="32656-524">阿洪姆語</span><span class="sxs-lookup"><span data-stu-id="32656-524">Ahom</span></span> |
| <span data-ttu-id="32656-525">Anatolian\_Hieroglyphs</span><span class="sxs-lookup"><span data-stu-id="32656-525">Anatolian\_Hieroglyphs</span></span> |
| <span data-ttu-id="32656-526">阿拉伯文</span><span class="sxs-lookup"><span data-stu-id="32656-526">Arabic</span></span> |
| <span data-ttu-id="32656-527">亞美尼亞文</span><span class="sxs-lookup"><span data-stu-id="32656-527">Armenian</span></span> |
| <span data-ttu-id="32656-528">阿維斯塔文</span><span class="sxs-lookup"><span data-stu-id="32656-528">Avestan</span></span> |
| <span data-ttu-id="32656-529">峇里文</span><span class="sxs-lookup"><span data-stu-id="32656-529">Balinese</span></span> |
| <span data-ttu-id="32656-530">巴姆文</span><span class="sxs-lookup"><span data-stu-id="32656-530">Bamum</span></span> |
| <span data-ttu-id="32656-531">Bassa\_Vah</span><span class="sxs-lookup"><span data-stu-id="32656-531">Bassa\_Vah</span></span> |
| <span data-ttu-id="32656-532">巴塔克文</span><span class="sxs-lookup"><span data-stu-id="32656-532">Batak</span></span> |
| <span data-ttu-id="32656-533">孟加拉文</span><span class="sxs-lookup"><span data-stu-id="32656-533">Bengali</span></span> |
| <span data-ttu-id="32656-534">拜克舒基文</span><span class="sxs-lookup"><span data-stu-id="32656-534">Bhaiksuki</span></span> |
| <span data-ttu-id="32656-535">注音符號</span><span class="sxs-lookup"><span data-stu-id="32656-535">Bopomofo</span></span> |
| <span data-ttu-id="32656-536">婆羅米文</span><span class="sxs-lookup"><span data-stu-id="32656-536">Brahmi</span></span> |
| <span data-ttu-id="32656-537">點字</span><span class="sxs-lookup"><span data-stu-id="32656-537">Braille</span></span> |
| <span data-ttu-id="32656-538">布吉斯文</span><span class="sxs-lookup"><span data-stu-id="32656-538">Buginese</span></span> |
| <span data-ttu-id="32656-539">布錫語</span><span class="sxs-lookup"><span data-stu-id="32656-539">Buhid</span></span> |
| <span data-ttu-id="32656-540">Canadian\_Aboriginal</span><span class="sxs-lookup"><span data-stu-id="32656-540">Canadian\_Aboriginal</span></span> |
| <span data-ttu-id="32656-541">卡里亞文</span><span class="sxs-lookup"><span data-stu-id="32656-541">Carian</span></span> |
| <span data-ttu-id="32656-542">Caucasian\_Albanian</span><span class="sxs-lookup"><span data-stu-id="32656-542">Caucasian\_Albanian</span></span> |
| <span data-ttu-id="32656-543">查克馬文</span><span class="sxs-lookup"><span data-stu-id="32656-543">Chakma</span></span> |
| <span data-ttu-id="32656-544">Cham</span><span class="sxs-lookup"><span data-stu-id="32656-544">Cham</span></span> |
| <span data-ttu-id="32656-545">卻洛奇文</span><span class="sxs-lookup"><span data-stu-id="32656-545">Cherokee</span></span> |
| <span data-ttu-id="32656-546">花剌子模語</span><span class="sxs-lookup"><span data-stu-id="32656-546">Chorasmian</span></span> |
| <span data-ttu-id="32656-547">通用</span><span class="sxs-lookup"><span data-stu-id="32656-547">Common</span></span> |
| <span data-ttu-id="32656-548">科普特語</span><span class="sxs-lookup"><span data-stu-id="32656-548">Coptic</span></span> |
| <span data-ttu-id="32656-549">楔形文字</span><span class="sxs-lookup"><span data-stu-id="32656-549">Cuneiform</span></span> |
| <span data-ttu-id="32656-550">賽普勒斯</span><span class="sxs-lookup"><span data-stu-id="32656-550">Cypriot</span></span> |
| <span data-ttu-id="32656-551">西里爾文</span><span class="sxs-lookup"><span data-stu-id="32656-551">Cyrillic</span></span> |
| <span data-ttu-id="32656-552">德瑟列特文</span><span class="sxs-lookup"><span data-stu-id="32656-552">Deseret</span></span> |
| <span data-ttu-id="32656-553">梵文字母</span><span class="sxs-lookup"><span data-stu-id="32656-553">Devanagari</span></span> |
| <span data-ttu-id="32656-554">Dives\_Akuru</span><span class="sxs-lookup"><span data-stu-id="32656-554">Dives\_Akuru</span></span> |
| <span data-ttu-id="32656-555">Dogra 文</span><span class="sxs-lookup"><span data-stu-id="32656-555">Dogra</span></span> |
| <span data-ttu-id="32656-556">杜普雷速记</span><span class="sxs-lookup"><span data-stu-id="32656-556">Duployan</span></span> |
| <span data-ttu-id="32656-557">Egyptian\_Hieroglyphs</span><span class="sxs-lookup"><span data-stu-id="32656-557">Egyptian\_Hieroglyphs</span></span> |
| <span data-ttu-id="32656-558">艾巴申語</span><span class="sxs-lookup"><span data-stu-id="32656-558">Elbasan</span></span> |
| <span data-ttu-id="32656-559">埃利邁文</span><span class="sxs-lookup"><span data-stu-id="32656-559">Elymaic</span></span> |
| <span data-ttu-id="32656-560">衣索比亞文</span><span class="sxs-lookup"><span data-stu-id="32656-560">Ethiopic</span></span> |
| <span data-ttu-id="32656-561">喬治亞文</span><span class="sxs-lookup"><span data-stu-id="32656-561">Georgian</span></span> |
| <span data-ttu-id="32656-562">格來哥利蒂克文</span><span class="sxs-lookup"><span data-stu-id="32656-562">Glagolitic</span></span> |
| <span data-ttu-id="32656-563">歌德</span><span class="sxs-lookup"><span data-stu-id="32656-563">Gothic</span></span> |
| <span data-ttu-id="32656-564">古蘭塔文</span><span class="sxs-lookup"><span data-stu-id="32656-564">Grantha</span></span> |
| <span data-ttu-id="32656-565">希臘文</span><span class="sxs-lookup"><span data-stu-id="32656-565">Greek</span></span> |
| <span data-ttu-id="32656-566">古吉拉特文</span><span class="sxs-lookup"><span data-stu-id="32656-566">Gujarati</span></span> |
| <span data-ttu-id="32656-567">Gunjala\_Gondi</span><span class="sxs-lookup"><span data-stu-id="32656-567">Gunjala\_Gondi</span></span> |
| <span data-ttu-id="32656-568">果魯穆奇文字</span><span class="sxs-lookup"><span data-stu-id="32656-568">Gurmukhi</span></span> |
| <span data-ttu-id="32656-569">漢語</span><span class="sxs-lookup"><span data-stu-id="32656-569">Han</span></span> |
| <span data-ttu-id="32656-570">諺文</span><span class="sxs-lookup"><span data-stu-id="32656-570">Hangul</span></span> |
| <span data-ttu-id="32656-571">Hanifi\_Rohingya</span><span class="sxs-lookup"><span data-stu-id="32656-571">Hanifi\_Rohingya</span></span> |
| <span data-ttu-id="32656-572">漢奴勞族文</span><span class="sxs-lookup"><span data-stu-id="32656-572">Hanunoo</span></span> |
| <span data-ttu-id="32656-573">哈特拉文</span><span class="sxs-lookup"><span data-stu-id="32656-573">Hatran</span></span> |
| <span data-ttu-id="32656-574">希伯來文</span><span class="sxs-lookup"><span data-stu-id="32656-574">Hebrew</span></span> |
| <span data-ttu-id="32656-575">平假名</span><span class="sxs-lookup"><span data-stu-id="32656-575">Hiragana</span></span> |
| <span data-ttu-id="32656-576">Imperial\_Aramaic</span><span class="sxs-lookup"><span data-stu-id="32656-576">Imperial\_Aramaic</span></span> |
| <span data-ttu-id="32656-577">已繼承</span><span class="sxs-lookup"><span data-stu-id="32656-577">Inherited</span></span> |
| <span data-ttu-id="32656-578">Inscriptional\_Pahlavi</span><span class="sxs-lookup"><span data-stu-id="32656-578">Inscriptional\_Pahlavi</span></span> |
| <span data-ttu-id="32656-579">Inscriptional\_Parthian</span><span class="sxs-lookup"><span data-stu-id="32656-579">Inscriptional\_Parthian</span></span> |
| <span data-ttu-id="32656-580">爪哇文</span><span class="sxs-lookup"><span data-stu-id="32656-580">Javanese</span></span> |
| <span data-ttu-id="32656-581">凱提體文</span><span class="sxs-lookup"><span data-stu-id="32656-581">Kaithi</span></span> |
| <span data-ttu-id="32656-582">坎那達文</span><span class="sxs-lookup"><span data-stu-id="32656-582">Kannada</span></span> |
| <span data-ttu-id="32656-583">片假名</span><span class="sxs-lookup"><span data-stu-id="32656-583">Katakana</span></span> |
| <span data-ttu-id="32656-584">Kayah\_Li</span><span class="sxs-lookup"><span data-stu-id="32656-584">Kayah\_Li</span></span> |
| <span data-ttu-id="32656-585">佉盧文</span><span class="sxs-lookup"><span data-stu-id="32656-585">Kharoshthi</span></span> |
| <span data-ttu-id="32656-586">Khitan\_Small\_Script</span><span class="sxs-lookup"><span data-stu-id="32656-586">Khitan\_Small\_Script</span></span> |
| <span data-ttu-id="32656-587">高棉文</span><span class="sxs-lookup"><span data-stu-id="32656-587">Khmer</span></span> |
| <span data-ttu-id="32656-588">郝吉文</span><span class="sxs-lookup"><span data-stu-id="32656-588">Khojki</span></span> |
| <span data-ttu-id="32656-589">信德文</span><span class="sxs-lookup"><span data-stu-id="32656-589">Khudawadi</span></span> |
| <span data-ttu-id="32656-590">寮文</span><span class="sxs-lookup"><span data-stu-id="32656-590">Lao</span></span> |
| <span data-ttu-id="32656-591">拉丁文</span><span class="sxs-lookup"><span data-stu-id="32656-591">Latin</span></span> |
| <span data-ttu-id="32656-592">雷布查文</span><span class="sxs-lookup"><span data-stu-id="32656-592">Lepcha</span></span> |
| <span data-ttu-id="32656-593">林布文</span><span class="sxs-lookup"><span data-stu-id="32656-593">Limbu</span></span> |
| <span data-ttu-id="32656-594">Linear\_A</span><span class="sxs-lookup"><span data-stu-id="32656-594">Linear\_A</span></span> |
| <span data-ttu-id="32656-595">Linear\_B</span><span class="sxs-lookup"><span data-stu-id="32656-595">Linear\_B</span></span> |
| <span data-ttu-id="32656-596">栗粟文</span><span class="sxs-lookup"><span data-stu-id="32656-596">Lisu</span></span> |
| <span data-ttu-id="32656-597">呂西亞文</span><span class="sxs-lookup"><span data-stu-id="32656-597">Lycian</span></span> |
| <span data-ttu-id="32656-598">利底亞文</span><span class="sxs-lookup"><span data-stu-id="32656-598">Lydian</span></span> |
| <span data-ttu-id="32656-599">馬哈加尼文</span><span class="sxs-lookup"><span data-stu-id="32656-599">Mahajani</span></span> |
| <span data-ttu-id="32656-600">瑪加沙文</span><span class="sxs-lookup"><span data-stu-id="32656-600">Makasar</span></span> |
| <span data-ttu-id="32656-601">馬來亞拉姆文</span><span class="sxs-lookup"><span data-stu-id="32656-601">Malayalam</span></span> |
| <span data-ttu-id="32656-602">曼底克文</span><span class="sxs-lookup"><span data-stu-id="32656-602">Mandaic</span></span> |
| <span data-ttu-id="32656-603">摩尼文</span><span class="sxs-lookup"><span data-stu-id="32656-603">Manichaean</span></span> |
| <span data-ttu-id="32656-604">Marchen 文</span><span class="sxs-lookup"><span data-stu-id="32656-604">Marchen</span></span> |
| <span data-ttu-id="32656-605">Masaram\_Gondi</span><span class="sxs-lookup"><span data-stu-id="32656-605">Masaram\_Gondi</span></span> |
| <span data-ttu-id="32656-606">梅德法伊德林文</span><span class="sxs-lookup"><span data-stu-id="32656-606">Medefaidrin</span></span> |
| <span data-ttu-id="32656-607">Meetei\_Mayek</span><span class="sxs-lookup"><span data-stu-id="32656-607">Meetei\_Mayek</span></span> |
| <span data-ttu-id="32656-608">Mende\_Kikakui</span><span class="sxs-lookup"><span data-stu-id="32656-608">Mende\_Kikakui</span></span> |
| <span data-ttu-id="32656-609">Meroitic\_Cursive</span><span class="sxs-lookup"><span data-stu-id="32656-609">Meroitic\_Cursive</span></span> |
| <span data-ttu-id="32656-610">Meroitic\_Hieroglyphs</span><span class="sxs-lookup"><span data-stu-id="32656-610">Meroitic\_Hieroglyphs</span></span> |
| <span data-ttu-id="32656-611">苗文</span><span class="sxs-lookup"><span data-stu-id="32656-611">Miao</span></span> |
| <span data-ttu-id="32656-612">Modi 文</span><span class="sxs-lookup"><span data-stu-id="32656-612">Modi</span></span> |
| <span data-ttu-id="32656-613">蒙古文</span><span class="sxs-lookup"><span data-stu-id="32656-613">Mongolian</span></span> |
| <span data-ttu-id="32656-614">姆諾文</span><span class="sxs-lookup"><span data-stu-id="32656-614">Mro</span></span> |
| <span data-ttu-id="32656-615">Multani 文</span><span class="sxs-lookup"><span data-stu-id="32656-615">Multani</span></span> |
| <span data-ttu-id="32656-616">緬甸</span><span class="sxs-lookup"><span data-stu-id="32656-616">Myanmar</span></span> |
| <span data-ttu-id="32656-617">納巴泰文</span><span class="sxs-lookup"><span data-stu-id="32656-617">Nabataean</span></span> |
| <span data-ttu-id="32656-618">南迪城文</span><span class="sxs-lookup"><span data-stu-id="32656-618">Nandinagari</span></span> |
| <span data-ttu-id="32656-619">New\_Tai\_Lue</span><span class="sxs-lookup"><span data-stu-id="32656-619">New\_Tai\_Lue</span></span> |
| <span data-ttu-id="32656-620">Newa 文</span><span class="sxs-lookup"><span data-stu-id="32656-620">Newa</span></span> |
| <span data-ttu-id="32656-621">西非書面文字</span><span class="sxs-lookup"><span data-stu-id="32656-621">Nko</span></span> |
| <span data-ttu-id="32656-622">女書</span><span class="sxs-lookup"><span data-stu-id="32656-622">Nushu</span></span> |
| <span data-ttu-id="32656-623">Nyiakeng\_Puachue\_Hmong</span><span class="sxs-lookup"><span data-stu-id="32656-623">Nyiakeng\_Puachue\_Hmong</span></span> |
| <span data-ttu-id="32656-624">歐甘字母</span><span class="sxs-lookup"><span data-stu-id="32656-624">Ogham</span></span> |
| <span data-ttu-id="32656-625">Ol\_Chiki</span><span class="sxs-lookup"><span data-stu-id="32656-625">Ol\_Chiki</span></span> |
| <span data-ttu-id="32656-626">Old\_Hungarian</span><span class="sxs-lookup"><span data-stu-id="32656-626">Old\_Hungarian</span></span> |
| <span data-ttu-id="32656-627">Old\_Italic</span><span class="sxs-lookup"><span data-stu-id="32656-627">Old\_Italic</span></span> |
| <span data-ttu-id="32656-628">Old\_North\_Arabian</span><span class="sxs-lookup"><span data-stu-id="32656-628">Old\_North\_Arabian</span></span> |
| <span data-ttu-id="32656-629">Old\_Permic</span><span class="sxs-lookup"><span data-stu-id="32656-629">Old\_Permic</span></span> |
| <span data-ttu-id="32656-630">Old\_Persian</span><span class="sxs-lookup"><span data-stu-id="32656-630">Old\_Persian</span></span> |
| <span data-ttu-id="32656-631">Old\_Sogdian</span><span class="sxs-lookup"><span data-stu-id="32656-631">Old\_Sogdian</span></span> |
| <span data-ttu-id="32656-632">Old\_South\_Arabian</span><span class="sxs-lookup"><span data-stu-id="32656-632">Old\_South\_Arabian</span></span> |
| <span data-ttu-id="32656-633">Old\_Turkic</span><span class="sxs-lookup"><span data-stu-id="32656-633">Old\_Turkic</span></span> |
| <span data-ttu-id="32656-634">奧里亞語</span><span class="sxs-lookup"><span data-stu-id="32656-634">Oriya</span></span> |
| <span data-ttu-id="32656-635">奧賽治文</span><span class="sxs-lookup"><span data-stu-id="32656-635">Osage</span></span> |
| <span data-ttu-id="32656-636">奧斯曼亞文</span><span class="sxs-lookup"><span data-stu-id="32656-636">Osmanya</span></span> |
| <span data-ttu-id="32656-637">Pahawh\_Hmong</span><span class="sxs-lookup"><span data-stu-id="32656-637">Pahawh\_Hmong</span></span> |
| <span data-ttu-id="32656-638">帕爾邁拉文</span><span class="sxs-lookup"><span data-stu-id="32656-638">Palmyrene</span></span> |
| <span data-ttu-id="32656-639">Pau\_Cin\_Hau</span><span class="sxs-lookup"><span data-stu-id="32656-639">Pau\_Cin\_Hau</span></span> |
| <span data-ttu-id="32656-640">Phags\_Pa</span><span class="sxs-lookup"><span data-stu-id="32656-640">Phags\_Pa</span></span> |
| <span data-ttu-id="32656-641">腓尼基文</span><span class="sxs-lookup"><span data-stu-id="32656-641">Phoenician</span></span> |
| <span data-ttu-id="32656-642">Psalter\_Pahlavi</span><span class="sxs-lookup"><span data-stu-id="32656-642">Psalter\_Pahlavi</span></span> |
| <span data-ttu-id="32656-643">拉讓文</span><span class="sxs-lookup"><span data-stu-id="32656-643">Rejang</span></span> |
| <span data-ttu-id="32656-644">盧恩文</span><span class="sxs-lookup"><span data-stu-id="32656-644">Runic</span></span> |
| <span data-ttu-id="32656-645">撒馬利亞文</span><span class="sxs-lookup"><span data-stu-id="32656-645">Samaritan</span></span> |
| <span data-ttu-id="32656-646">紹拉斯徹文</span><span class="sxs-lookup"><span data-stu-id="32656-646">Saurashtra</span></span> |
| <span data-ttu-id="32656-647">沙拉達文</span><span class="sxs-lookup"><span data-stu-id="32656-647">Sharada</span></span> |
| <span data-ttu-id="32656-648">蕭伯納文</span><span class="sxs-lookup"><span data-stu-id="32656-648">Shavian</span></span> |
| <span data-ttu-id="32656-649">悉曇文</span><span class="sxs-lookup"><span data-stu-id="32656-649">Siddham</span></span> |
| <span data-ttu-id="32656-650">手語書寫</span><span class="sxs-lookup"><span data-stu-id="32656-650">SignWriting</span></span> |
| <span data-ttu-id="32656-651">僧伽羅文</span><span class="sxs-lookup"><span data-stu-id="32656-651">Sinhala</span></span> |
| <span data-ttu-id="32656-652">粟特文</span><span class="sxs-lookup"><span data-stu-id="32656-652">Sogdian</span></span> |
| <span data-ttu-id="32656-653">Sora\_Sompeng</span><span class="sxs-lookup"><span data-stu-id="32656-653">Sora\_Sompeng</span></span> |
| <span data-ttu-id="32656-654">索永布文</span><span class="sxs-lookup"><span data-stu-id="32656-654">Soyombo</span></span> |
| <span data-ttu-id="32656-655">巽丹文</span><span class="sxs-lookup"><span data-stu-id="32656-655">Sundanese</span></span> |
| <span data-ttu-id="32656-656">Syloti\_Nagri</span><span class="sxs-lookup"><span data-stu-id="32656-656">Syloti\_Nagri</span></span> |
| <span data-ttu-id="32656-657">敘利亞文</span><span class="sxs-lookup"><span data-stu-id="32656-657">Syriac</span></span> |
| <span data-ttu-id="32656-658">他加祿語</span><span class="sxs-lookup"><span data-stu-id="32656-658">Tagalog</span></span> |
| <span data-ttu-id="32656-659">塔班瓦語</span><span class="sxs-lookup"><span data-stu-id="32656-659">Tagbanwa</span></span> |
| <span data-ttu-id="32656-660">Tai\_Le</span><span class="sxs-lookup"><span data-stu-id="32656-660">Tai\_Le</span></span> |
| <span data-ttu-id="32656-661">Tai\_Tham</span><span class="sxs-lookup"><span data-stu-id="32656-661">Tai\_Tham</span></span> |
| <span data-ttu-id="32656-662">Tai\_Viet</span><span class="sxs-lookup"><span data-stu-id="32656-662">Tai\_Viet</span></span> |
| <span data-ttu-id="32656-663">塔卡里文</span><span class="sxs-lookup"><span data-stu-id="32656-663">Takri</span></span> |
| <span data-ttu-id="32656-664">坦米爾文</span><span class="sxs-lookup"><span data-stu-id="32656-664">Tamil</span></span> |
| <span data-ttu-id="32656-665">西夏語</span><span class="sxs-lookup"><span data-stu-id="32656-665">Tangut</span></span> |
| <span data-ttu-id="32656-666">特拉古文</span><span class="sxs-lookup"><span data-stu-id="32656-666">Telugu</span></span> |
| <span data-ttu-id="32656-667">塔安那文</span><span class="sxs-lookup"><span data-stu-id="32656-667">Thaana</span></span> |
| <span data-ttu-id="32656-668">泰文</span><span class="sxs-lookup"><span data-stu-id="32656-668">Thai</span></span> |
| <span data-ttu-id="32656-669">藏文</span><span class="sxs-lookup"><span data-stu-id="32656-669">Tibetan</span></span> |
| <span data-ttu-id="32656-670">提弗納文</span><span class="sxs-lookup"><span data-stu-id="32656-670">Tifinagh</span></span> |
| <span data-ttu-id="32656-671">底羅仆多文</span><span class="sxs-lookup"><span data-stu-id="32656-671">Tirhuta</span></span> |
| <span data-ttu-id="32656-672">烏加里特語</span><span class="sxs-lookup"><span data-stu-id="32656-672">Ugaritic</span></span> |
| <span data-ttu-id="32656-673">范文</span><span class="sxs-lookup"><span data-stu-id="32656-673">Vai</span></span> |
| <span data-ttu-id="32656-674">Wancho 語</span><span class="sxs-lookup"><span data-stu-id="32656-674">Wancho</span></span> |
| <span data-ttu-id="32656-675">Warang\_Citi</span><span class="sxs-lookup"><span data-stu-id="32656-675">Warang\_Citi</span></span> |
| <span data-ttu-id="32656-676">亞茲迪文</span><span class="sxs-lookup"><span data-stu-id="32656-676">Yezidi</span></span> |
| <span data-ttu-id="32656-677">彝文</span><span class="sxs-lookup"><span data-stu-id="32656-677">Yi</span></span> |
| <span data-ttu-id="32656-678">Zanabazar\_Square</span><span class="sxs-lookup"><span data-stu-id="32656-678">Zanabazar\_Square</span></span> |

|&nbsp;| <span data-ttu-id="32656-679">Vim 字元類別</span><span class="sxs-lookup"><span data-stu-id="32656-679">Vim character classes</span></span> |
| --- | --- |
| <span data-ttu-id="32656-680">\i</span><span class="sxs-lookup"><span data-stu-id="32656-680">\i</span></span> | <span data-ttu-id="32656-681">識別碼字元 FF (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-681">identifier character (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-682">\I</span><span class="sxs-lookup"><span data-stu-id="32656-682">\I</span></span> | <span data-ttu-id="32656-683">\i 排除數字 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-683">\i except digits (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-684">\k</span><span class="sxs-lookup"><span data-stu-id="32656-684">\k</span></span> | <span data-ttu-id="32656-685">關鍵字字元 FF (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-685">keyword character (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-686">\K</span><span class="sxs-lookup"><span data-stu-id="32656-686">\K</span></span> | <span data-ttu-id="32656-687">\k 排除數字 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-687">\k except digits (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-688">\f</span><span class="sxs-lookup"><span data-stu-id="32656-688">\f</span></span> | <span data-ttu-id="32656-689">檔案名字元 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-689">file name character (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-690">\F</span><span class="sxs-lookup"><span data-stu-id="32656-690">\F</span></span> | <span data-ttu-id="32656-691">\f 排除數字 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-691">\f except digits (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-692">\p</span><span class="sxs-lookup"><span data-stu-id="32656-692">\p</span></span> | <span data-ttu-id="32656-693">可列印字元 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-693">printable character (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-694">\P</span><span class="sxs-lookup"><span data-stu-id="32656-694">\P</span></span> | <span data-ttu-id="32656-695">\p 排除數字 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-695">\p except digits (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-696">\s</span><span class="sxs-lookup"><span data-stu-id="32656-696">\s</span></span> | <span data-ttu-id="32656-697">空格字元 (≡ [\t]) (NOT SUPPORTED) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-697">whitespace character (≡ [\t]) (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-698">\S</span><span class="sxs-lookup"><span data-stu-id="32656-698">\S</span></span> | <span data-ttu-id="32656-699">非空格字元 (≡ [^ \t]) (NOT SUPPORTED) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-699">non-white space character (≡ [^ \t]) (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-700">\d</span><span class="sxs-lookup"><span data-stu-id="32656-700">\d</span></span> | <span data-ttu-id="32656-701">数位 (≡ [0-9]) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-701">digits (≡ [0-9]) VIM</span></span> |
| <span data-ttu-id="32656-702">\D</span><span class="sxs-lookup"><span data-stu-id="32656-702">\D</span></span> | <span data-ttu-id="32656-703">非 \d VIM</span><span class="sxs-lookup"><span data-stu-id="32656-703">not \d VIM</span></span> |
| <span data-ttu-id="32656-704">\x</span><span class="sxs-lookup"><span data-stu-id="32656-704">\x</span></span> | <span data-ttu-id="32656-705">十六進位數位 (≡ [0-9A-Fa-f]) (NOT SUPPORTED) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-705">hex digits (≡ [0-9A-Fa-f]) (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-706">\X</span><span class="sxs-lookup"><span data-stu-id="32656-706">\X</span></span> | <span data-ttu-id="32656-707">非 \x (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-707">not \x (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-708">\o</span><span class="sxs-lookup"><span data-stu-id="32656-708">\o</span></span> | <span data-ttu-id="32656-709">八進位數位 (≡ [0-7]) (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-709">octal digits (≡ [0-7]) (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-710">\O</span><span class="sxs-lookup"><span data-stu-id="32656-710">\O</span></span> | <span data-ttu-id="32656-711">非 \o (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-711">not \o (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-712">\w</span><span class="sxs-lookup"><span data-stu-id="32656-712">\w</span></span> | <span data-ttu-id="32656-713">文字字元 VIM</span><span class="sxs-lookup"><span data-stu-id="32656-713">word character VIM</span></span> |
| <span data-ttu-id="32656-714">\W</span><span class="sxs-lookup"><span data-stu-id="32656-714">\W</span></span> | <span data-ttu-id="32656-715">非 \w VIM</span><span class="sxs-lookup"><span data-stu-id="32656-715">not \w VIM</span></span> |
| <span data-ttu-id="32656-716">\h</span><span class="sxs-lookup"><span data-stu-id="32656-716">\h</span></span> | <span data-ttu-id="32656-717">文字字元標題 FF (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-717">head of word character (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-718">\H</span><span class="sxs-lookup"><span data-stu-id="32656-718">\H</span></span> | <span data-ttu-id="32656-719">非 \h (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-719">not \h (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-720">\a</span><span class="sxs-lookup"><span data-stu-id="32656-720">\a</span></span> | <span data-ttu-id="32656-721">字母 \o (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-721">alphabetic (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-722">\A</span><span class="sxs-lookup"><span data-stu-id="32656-722">\A</span></span> | <span data-ttu-id="32656-723">非 \a (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-723">not \a (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-724">\l</span><span class="sxs-lookup"><span data-stu-id="32656-724">\l</span></span> | <span data-ttu-id="32656-725">小寫 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-725">lowercase (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-726">\L</span><span class="sxs-lookup"><span data-stu-id="32656-726">\L</span></span> | <span data-ttu-id="32656-727">非小寫 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-727">not lowercase (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-728">\u</span><span class="sxs-lookup"><span data-stu-id="32656-728">\u</span></span> | <span data-ttu-id="32656-729">大寫 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-729">uppercase (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-730">\U</span><span class="sxs-lookup"><span data-stu-id="32656-730">\U</span></span> | <span data-ttu-id="32656-731">非大寫 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-731">not uppercase (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-732">\_x</span><span class="sxs-lookup"><span data-stu-id="32656-732">\_x</span></span> | <span data-ttu-id="32656-733">\x 和分行符號，適用于任何 x (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-733">\x plus newline, for any x (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-734">\c</span><span class="sxs-lookup"><span data-stu-id="32656-734">\c</span></span> | <span data-ttu-id="32656-735">忽略大小寫 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-735">ignore case (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-736">\C</span><span class="sxs-lookup"><span data-stu-id="32656-736">\C</span></span> | <span data-ttu-id="32656-737">符合大小寫 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-737">match case (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-738">\m</span><span class="sxs-lookup"><span data-stu-id="32656-738">\m</span></span> | <span data-ttu-id="32656-739">魔術 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-739">magic (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-740">\M</span><span class="sxs-lookup"><span data-stu-id="32656-740">\M</span></span> | <span data-ttu-id="32656-741">非魔術 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-741">nomagic (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-742">\v</span><span class="sxs-lookup"><span data-stu-id="32656-742">\v</span></span> | <span data-ttu-id="32656-743">超魔術 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-743">verymagic (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-744">\V</span><span class="sxs-lookup"><span data-stu-id="32656-744">\V</span></span> | <span data-ttu-id="32656-745">超非魔術 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-745">verynomagic (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="32656-746">\Z</span><span class="sxs-lookup"><span data-stu-id="32656-746">\Z</span></span> | <span data-ttu-id="32656-747">忽略 Unicode 結合字元中的差異 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="32656-747">ignore differences in Unicode combining characters (NOT SUPPORTED) VIM</span></span> |

| &nbsp; | <span data-ttu-id="32656-748">魔術</span><span class="sxs-lookup"><span data-stu-id="32656-748">Magic</span></span> |
| --- | --- |
| <span data-ttu-id="32656-749">(?{code})</span><span class="sxs-lookup"><span data-stu-id="32656-749">(?{code})</span></span> | <span data-ttu-id="32656-750">任意 Perl 代碼 (不支援) PERL</span><span class="sxs-lookup"><span data-stu-id="32656-750">arbitrary Perl code (NOT SUPPORTED) PERL</span></span> |
| <span data-ttu-id="32656-751">(??{code})</span><span class="sxs-lookup"><span data-stu-id="32656-751">(??{code})</span></span> | <span data-ttu-id="32656-752">已延遲任意 Perl 代碼 (不支援) PERL</span><span class="sxs-lookup"><span data-stu-id="32656-752">postponed arbitrary Perl code (NOT SUPPORTED) PERL</span></span> |
| <span data-ttu-id="32656-753">(?n)</span><span class="sxs-lookup"><span data-stu-id="32656-753">(?n)</span></span> | <span data-ttu-id="32656-754">對 regexp 擷取群組 n 的遞迴撥號 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-754">recursive call to regexp capturing group n (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-755">(?+n)</span><span class="sxs-lookup"><span data-stu-id="32656-755">(?+n)</span></span> | <span data-ttu-id="32656-756">遞迴呼叫相關群組 +n (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-756">recursive call to relative group +n (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-757">(?-n)</span><span class="sxs-lookup"><span data-stu-id="32656-757">(?-n)</span></span> | <span data-ttu-id="32656-758">遞迴呼叫相關群組 -n (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-758">recursive call to relative group -n (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-759">(?C)</span><span class="sxs-lookup"><span data-stu-id="32656-759">(?C)</span></span> | <span data-ttu-id="32656-760">PCRE 圖說文字 (不支援) PCRE</span><span class="sxs-lookup"><span data-stu-id="32656-760">PCRE callout (NOT SUPPORTED) PCRE</span></span> |
| <span data-ttu-id="32656-761">(?R)</span><span class="sxs-lookup"><span data-stu-id="32656-761">(?R)</span></span> | <span data-ttu-id="32656-762">對整個 regexp 的遞迴撥號 (≡ (?0)) (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-762">recursive call to entire regexp (≡ (?0)) (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-763">(?&amp;name)</span><span class="sxs-lookup"><span data-stu-id="32656-763">(?&amp;name)</span></span> | <span data-ttu-id="32656-764">遞迴呼叫具名群組 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-764">recursive call to named group (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-765">(?P=name)</span><span class="sxs-lookup"><span data-stu-id="32656-765">(?P=name)</span></span> | <span data-ttu-id="32656-766">具名反向參考 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-766">named backreference (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-767">(?P&gt;name)</span><span class="sxs-lookup"><span data-stu-id="32656-767">(?P&gt;name)</span></span> | <span data-ttu-id="32656-768">遞迴呼叫具名群組 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-768">recursive call to named group (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-769">(?(cond)true</span><span class="sxs-lookup"><span data-stu-id="32656-769">(?(cond)true</span></span>|<span data-ttu-id="32656-770">false)</span><span class="sxs-lookup"><span data-stu-id="32656-770">false)</span></span> | <span data-ttu-id="32656-771">條件式分支 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-771">conditional branch (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-772">(?(cond)true)</span><span class="sxs-lookup"><span data-stu-id="32656-772">(?(cond)true)</span></span> | <span data-ttu-id="32656-773">條件式分支 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-773">conditional branch (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-774">(\*ACCEPT)</span><span class="sxs-lookup"><span data-stu-id="32656-774">(\*ACCEPT)</span></span> | <span data-ttu-id="32656-775">讓 regexps 更像 Prolog (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-775">make regexps more like Prolog (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-776">(\*COMMIT)</span><span class="sxs-lookup"><span data-stu-id="32656-776">(\*COMMIT)</span></span> | <span data-ttu-id="32656-777">(不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-777">(NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-778">(\*F)</span><span class="sxs-lookup"><span data-stu-id="32656-778">(\*F)</span></span> | <span data-ttu-id="32656-779">(不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-779">(NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-780">(\*FAIL)</span><span class="sxs-lookup"><span data-stu-id="32656-780">(\*FAIL)</span></span> | <span data-ttu-id="32656-781">(不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-781">(NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-782">(\*MARK)</span><span class="sxs-lookup"><span data-stu-id="32656-782">(\*MARK)</span></span> | <span data-ttu-id="32656-783">(不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-783">(NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-784">(\*PRUNE)</span><span class="sxs-lookup"><span data-stu-id="32656-784">(\*PRUNE)</span></span> | <span data-ttu-id="32656-785">(不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-785">(NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-786">(\*SKIP)</span><span class="sxs-lookup"><span data-stu-id="32656-786">(\*SKIP)</span></span> | <span data-ttu-id="32656-787">(不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-787">(NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-788">(\*THEN)</span><span class="sxs-lookup"><span data-stu-id="32656-788">(\*THEN)</span></span> | <span data-ttu-id="32656-789">(不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-789">(NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-790">(\*ANY)</span><span class="sxs-lookup"><span data-stu-id="32656-790">(\*ANY)</span></span> | <span data-ttu-id="32656-791">設定分行符號慣例 (不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-791">set newline convention (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-792">(\*ANYCRLF)</span><span class="sxs-lookup"><span data-stu-id="32656-792">(\*ANYCRLF)</span></span> | <span data-ttu-id="32656-793">(不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-793">(NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-794">(\*CR)</span><span class="sxs-lookup"><span data-stu-id="32656-794">(\*CR)</span></span> | <span data-ttu-id="32656-795">(不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-795">(NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-796">(\*CRLF)</span><span class="sxs-lookup"><span data-stu-id="32656-796">(\*CRLF)</span></span> | <span data-ttu-id="32656-797">(不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-797">(NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-798">(\*LF)</span><span class="sxs-lookup"><span data-stu-id="32656-798">(\*LF)</span></span> | <span data-ttu-id="32656-799">(不支援)</span><span class="sxs-lookup"><span data-stu-id="32656-799">(NOT SUPPORTED)</span></span> |
| <span data-ttu-id="32656-800">(\*BSR\_ANYCRLF)</span><span class="sxs-lookup"><span data-stu-id="32656-800">(\*BSR\_ANYCRLF)</span></span> | <span data-ttu-id="32656-801">設定 \R 慣例 (不支援) PCRE</span><span class="sxs-lookup"><span data-stu-id="32656-801">set \R convention (NOT SUPPORTED) PCRE</span></span> |
| <span data-ttu-id="32656-802">(\*BSR\_UNICODE)</span><span class="sxs-lookup"><span data-stu-id="32656-802">(\*BSR\_UNICODE)</span></span> | <span data-ttu-id="32656-803">(不支援) PCRE</span><span class="sxs-lookup"><span data-stu-id="32656-803">(NOT SUPPORTED) PCRE</span></span> |

## <a name="content-license"></a><span data-ttu-id="32656-804">內容授權</span><span class="sxs-lookup"><span data-stu-id="32656-804">Content license</span></span>

> [!NOTE]
> <span data-ttu-id="32656-805">本頁的某些部分是根據 Chromium.org 創造和分享的作品加以修改，並根據[創用 CC 姓名標示 4.0 國際版本授權條款](http://creativecommons.org/licenses/by/4.0/)中所述條款加以使用。</span><span class="sxs-lookup"><span data-stu-id="32656-805">Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span></span> <span data-ttu-id="32656-806">原始頁面可在[此處](https://github.com/google/re2/wiki/Syntax)找到。</span><span class="sxs-lookup"><span data-stu-id="32656-806">The original page can be found [here](https://github.com/google/re2/wiki/Syntax).</span></span>
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span data-ttu-id="32656-807">本作品根據<a rel="license" href="http://creativecommons.org/licenses/by/4.0/">創用 CC 姓名標示 4.0 國際版本授權條款</a>獲得授權。</span><span class="sxs-lookup"><span data-stu-id="32656-807">This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span></span>

## <a name="see-also"></a><span data-ttu-id="32656-808">請參閱</span><span class="sxs-lookup"><span data-stu-id="32656-808">See also</span></span>

- [<span data-ttu-id="32656-809">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="32656-809">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)